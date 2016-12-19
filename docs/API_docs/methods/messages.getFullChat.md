## Method: messages.getFullChat  

### Parameters:

| Name     |    Type       | Required |
|----------|:-------------:|---------:|
|chat\_id|[int](../types/int.md) | Required|


### Return type: [messages\_ChatFull](../types/messages\_ChatFull.md)

### Example:


```
$MadelineProto = new \danog\MadelineProto\API();
if (isset($token)) {
    $this->bot_login($token);
}
if (isset($number)) {
    $sentCode = $MadelineProto->phone_login($number);
    echo 'Enter the code you received: ';
    $code = '';
    for ($x = 0; $x < $sentCode['type']['length']; $x++) {
        $code .= fgetc(STDIN);
    }
    $MadelineProto->complete_phone_login($code);
}

$messages_ChatFull = $MadelineProto->messages->getFullChat(['chat_id' => int, ]);
```
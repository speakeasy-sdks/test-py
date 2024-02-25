# Pets


### Available Operations

* [createPets](#createpets) - Create a pet
* [listPets](#listpets) - List all pets
* [showPetById](#showpetbyid) - Info for a specific pet

## createPets

Create a pet

### Example Usage

```php
<?php

declare(strict_types=1);

require 'vendor/autoload.php';

use \next_test\a;

$sdk = a\A::builder()->build();

try {
    $response = $sdk->pets->createPets();

    if ($response->statusCode === 200) {
        // handle response
    }
} catch (Throwable $e) {
    // handle exception
}
```


### Response

**[?\next_test\a\Models\Operations\CreatePetsResponse](../../Models/Operations/CreatePetsResponse.md)**


## listPets

List all pets

### Example Usage

```php
<?php

declare(strict_types=1);

require 'vendor/autoload.php';

use \next_test\a;
use \next_test\a\Models\Operations;

$sdk = a\A::builder()->build();

try {
        $request = new Operations\ListPetsRequest();
    $request->limit = 21453;;

    $response = $sdk->pets->listPets($request);

    if ($response->pets !== null) {
        // handle response
    }
} catch (Throwable $e) {
    // handle exception
}
```

### Parameters

| Parameter                                                                                    | Type                                                                                         | Required                                                                                     | Description                                                                                  |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `$request`                                                                                   | [\next_test\a\Models\Operations\ListPetsRequest](../../Models/Operations/ListPetsRequest.md) | :heavy_check_mark:                                                                           | The request object to use for the request.                                                   |


### Response

**[?\next_test\a\Models\Operations\ListPetsResponse](../../Models/Operations/ListPetsResponse.md)**


## showPetById

Info for a specific pet

### Example Usage

```php
<?php

declare(strict_types=1);

require 'vendor/autoload.php';

use \next_test\a;
use \next_test\a\Models\Operations;

$sdk = a\A::builder()->build();

try {
        $request = new Operations\ShowPetByIdRequest();
    $request->petId = '<value>';;

    $response = $sdk->pets->showPetById($request);

    if ($response->pet !== null) {
        // handle response
    }
} catch (Throwable $e) {
    // handle exception
}
```

### Parameters

| Parameter                                                                                          | Type                                                                                               | Required                                                                                           | Description                                                                                        |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `$request`                                                                                         | [\next_test\a\Models\Operations\ShowPetByIdRequest](../../Models/Operations/ShowPetByIdRequest.md) | :heavy_check_mark:                                                                                 | The request object to use for the request.                                                         |


### Response

**[?\next_test\a\Models\Operations\ShowPetByIdResponse](../../Models/Operations/ShowPetByIdResponse.md)**


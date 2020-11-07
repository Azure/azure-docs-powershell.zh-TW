---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BF054CA4-B0A4-4BFC-A657-92A0D3ABBCB5
online version: ''
schema: 2.0.0
ms.openlocfilehash: f82db6a826a6ed612e1d98c7cef6ab642bf15858
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966997"
---
# <span data-ttu-id="5328a-101">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="5328a-101">Get-AzureStorSimpleStorageAccountCredential</span></span>

## <span data-ttu-id="5328a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5328a-102">SYNOPSIS</span></span>
<span data-ttu-id="5328a-103">取得儲存空間帳戶的認證。</span><span class="sxs-lookup"><span data-stu-id="5328a-103">Gets credentials for storage accounts.</span></span>

## <span data-ttu-id="5328a-104">句法</span><span class="sxs-lookup"><span data-stu-id="5328a-104">SYNTAX</span></span>

```
Get-AzureStorSimpleStorageAccountCredential [-StorageAccountName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="5328a-105">說明</span><span class="sxs-lookup"><span data-stu-id="5328a-105">DESCRIPTION</span></span>
<span data-ttu-id="5328a-106">**AzureStorSimpleStorageAccountCredential** Cmdlet 會取得儲存空間帳戶的認證。</span><span class="sxs-lookup"><span data-stu-id="5328a-106">The **Get-AzureStorSimpleStorageAccountCredential** cmdlet gets credentials for storage accounts.</span></span>
<span data-ttu-id="5328a-107">這個 Cmdlet 會取得在服務或命名 **StorageAccountCredential** 中設定的所有 **StorageAccountCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="5328a-107">This cmdlet gets all **StorageAccountCredential** objects configured in the service or a named **StorageAccountCredential**.</span></span>

## <span data-ttu-id="5328a-108">示例</span><span class="sxs-lookup"><span data-stu-id="5328a-108">EXAMPLES</span></span>

### <span data-ttu-id="5328a-109">範例1：取得資源的所有認證</span><span class="sxs-lookup"><span data-stu-id="5328a-109">Example 1: Get all credentials for a resource</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential
InstanceId                           Login           Name            UseSSL VolumeCount     CloudType    Location
----------                           -----           ----            ------ -----------     ---------    --------
b5e0857f-82ef-4426-883b-a612889ebee4 qwertyuiopa     AdminAccount    True   24              Azure
```

<span data-ttu-id="5328a-110">這個命令會取得目前資源之儲存空間帳戶的所有可用認證。</span><span class="sxs-lookup"><span data-stu-id="5328a-110">This command gets all available credentials for storage accounts for the current resource.</span></span>

### <span data-ttu-id="5328a-111">範例2：取得特定儲存空間帳戶的認證</span><span class="sxs-lookup"><span data-stu-id="5328a-111">Example 2: Get the credential for a specific storage account</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoCloudStorage"
VERBOSE: ClientRequestId: 16551af6-3398-4d30-a389-1b8eb01ce92c_PS
VERBOSE: ClientRequestId: 5041277d-4044-4b6c-ae19-4ea9e7ae135a_PS
VERBOSE: Storage Access Credential with name ContosoCloudStorage found! 


CloudType                        : Azure
Hostname                         : blob.core.windows.net
InstanceId                       : 8b3cb7bb-963b-4173-9598-52fe230b0350
IsDefault                        : False
Location                         : West US
Login                            : ContosoCloudStorage
Name                             : ContosoCloudStorage
OperationInProgress              : None
Password                         : 
PasswordEncryptionCertThumbprint : 
UseSSL                           : True
VolumeCount                      : 0
```

<span data-ttu-id="5328a-112">這個命令會取得名為 ContosoCloudStorage 之儲存帳戶的儲存空間帳號憑證。</span><span class="sxs-lookup"><span data-stu-id="5328a-112">This command gets the storage account credential for the storage account named ContosoCloudStorage.</span></span>

## <span data-ttu-id="5328a-113">參數</span><span class="sxs-lookup"><span data-stu-id="5328a-113">PARAMETERS</span></span>

### <span data-ttu-id="5328a-114">-設定檔</span><span class="sxs-lookup"><span data-stu-id="5328a-114">-Profile</span></span>
<span data-ttu-id="5328a-115">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="5328a-115">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5328a-116">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5328a-116">-StorageAccountName</span></span>
<span data-ttu-id="5328a-117">指定要取得認證的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="5328a-117">Specifies the name of the storage account for which to get credentials.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5328a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5328a-118">CommonParameters</span></span>
<span data-ttu-id="5328a-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5328a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5328a-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5328a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5328a-121">輸入</span><span class="sxs-lookup"><span data-stu-id="5328a-121">INPUTS</span></span>

### <span data-ttu-id="5328a-122">所有</span><span class="sxs-lookup"><span data-stu-id="5328a-122">None</span></span>

## <span data-ttu-id="5328a-123">輸出</span><span class="sxs-lookup"><span data-stu-id="5328a-123">OUTPUTS</span></span>

### <span data-ttu-id="5328a-124">StorageAccountCredential、IList\<StorageAccountCredential\></span><span class="sxs-lookup"><span data-stu-id="5328a-124">StorageAccountCredential, IList\<StorageAccountCredential\></span></span>
<span data-ttu-id="5328a-125">這個 Cmdlet 會傳回 **StorageAccountCredential** 物件，如果您指定 *StorageAccountName* 參數，或者如果您不指定該參數，則會傳回 **IList \<StorageAccountCredential\>** 物件。</span><span class="sxs-lookup"><span data-stu-id="5328a-125">This cmdlet returns a **StorageAccountCredential** object, if you specify the *StorageAccountName* parameter, or if you do not specify that parameter, it returns an **IList\<StorageAccountCredential\>** object.</span></span>

## <span data-ttu-id="5328a-126">筆記</span><span class="sxs-lookup"><span data-stu-id="5328a-126">NOTES</span></span>

## <span data-ttu-id="5328a-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="5328a-127">RELATED LINKS</span></span>

[<span data-ttu-id="5328a-128">新-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="5328a-128">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="5328a-129">移除-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="5328a-129">Remove-AzureStorSimpleStorageAccountCredential</span></span>](./Remove-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="5328a-130">Set-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="5328a-130">Set-AzureStorSimpleStorageAccountCredential</span></span>](./Set-AzureStorSimpleStorageAccountCredential.md)



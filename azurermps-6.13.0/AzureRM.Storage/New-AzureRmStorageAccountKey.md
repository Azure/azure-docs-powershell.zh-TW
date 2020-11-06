---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/new-azurermstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
ms.openlocfilehash: e44ccbaae730554db35610ff1084e9740e873e53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455912"
---
# <span data-ttu-id="9c395-101">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="9c395-101">New-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="9c395-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9c395-102">SYNOPSIS</span></span>
<span data-ttu-id="9c395-103">重新產生 Azure 儲存空間帳戶的儲存金鑰。</span><span class="sxs-lookup"><span data-stu-id="9c395-103">Regenerates a storage key for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c395-104">句法</span><span class="sxs-lookup"><span data-stu-id="9c395-104">SYNTAX</span></span>

```
New-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c395-105">說明</span><span class="sxs-lookup"><span data-stu-id="9c395-105">DESCRIPTION</span></span>
<span data-ttu-id="9c395-106">**新的-AzureRmStorageAccountKey** Cmdlet 會為 Azure 儲存空間帳戶重新產生儲存空間金鑰。</span><span class="sxs-lookup"><span data-stu-id="9c395-106">The **New-AzureRmStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="9c395-107">示例</span><span class="sxs-lookup"><span data-stu-id="9c395-107">EXAMPLES</span></span>

### <span data-ttu-id="9c395-108">範例1：重新產生儲存金鑰</span><span class="sxs-lookup"><span data-stu-id="9c395-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzureRmStorageKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="9c395-109">這個命令會為指定的儲存空間帳戶重新生成儲存空間。</span><span class="sxs-lookup"><span data-stu-id="9c395-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="9c395-110">參數</span><span class="sxs-lookup"><span data-stu-id="9c395-110">PARAMETERS</span></span>

### <span data-ttu-id="9c395-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c395-111">-DefaultProfile</span></span>
<span data-ttu-id="9c395-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9c395-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c395-113">-KeyName</span><span class="sxs-lookup"><span data-stu-id="9c395-113">-KeyName</span></span>
<span data-ttu-id="9c395-114">指定要重新產生的金鑰。</span><span class="sxs-lookup"><span data-stu-id="9c395-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="9c395-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="9c395-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9c395-116">key1</span><span class="sxs-lookup"><span data-stu-id="9c395-116">key1</span></span>
- <span data-ttu-id="9c395-117">key2</span><span class="sxs-lookup"><span data-stu-id="9c395-117">key2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c395-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="9c395-118">-Name</span></span>
<span data-ttu-id="9c395-119">指定要重新產生儲存金鑰的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="9c395-119">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c395-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c395-120">-ResourceGroupName</span></span>
<span data-ttu-id="9c395-121">指定包含儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c395-121">Specifies the name of the resource group that contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c395-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c395-122">CommonParameters</span></span>
<span data-ttu-id="9c395-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9c395-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c395-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9c395-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c395-125">輸入</span><span class="sxs-lookup"><span data-stu-id="9c395-125">INPUTS</span></span>

### <span data-ttu-id="9c395-126">System.object</span><span class="sxs-lookup"><span data-stu-id="9c395-126">System.String</span></span>

## <span data-ttu-id="9c395-127">輸出</span><span class="sxs-lookup"><span data-stu-id="9c395-127">OUTPUTS</span></span>

### <span data-ttu-id="9c395-128">StorageAccountKey （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="9c395-128">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="9c395-129">筆記</span><span class="sxs-lookup"><span data-stu-id="9c395-129">NOTES</span></span>

## <span data-ttu-id="9c395-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="9c395-130">RELATED LINKS</span></span>

[<span data-ttu-id="9c395-131">AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="9c395-131">Get-AzureRmStorageAccountKey</span></span>](./Get-AzureRmStorageAccountKey.md)

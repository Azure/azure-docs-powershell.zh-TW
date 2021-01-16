---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: eebf58120449466ac18231af6daed538ff7da937
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280107"
---
# <span data-ttu-id="a28b9-101">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a28b9-101">New-AzStorageAccountKey</span></span>

## <span data-ttu-id="a28b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a28b9-102">SYNOPSIS</span></span>
<span data-ttu-id="a28b9-103">重新產生 Azure 儲存空間帳戶的儲存金鑰。</span><span class="sxs-lookup"><span data-stu-id="a28b9-103">Regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="a28b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="a28b9-104">SYNTAX</span></span>

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a28b9-105">說明</span><span class="sxs-lookup"><span data-stu-id="a28b9-105">DESCRIPTION</span></span>
<span data-ttu-id="a28b9-106">**新的-AzStorageAccountKey** Cmdlet 會為 Azure 儲存空間帳戶重新產生儲存空間金鑰。</span><span class="sxs-lookup"><span data-stu-id="a28b9-106">The **New-AzStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="a28b9-107">示例</span><span class="sxs-lookup"><span data-stu-id="a28b9-107">EXAMPLES</span></span>

### <span data-ttu-id="a28b9-108">範例1：重新產生儲存金鑰</span><span class="sxs-lookup"><span data-stu-id="a28b9-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzStorageAccountKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="a28b9-109">這個命令會為指定的儲存空間帳戶重新生成儲存空間。</span><span class="sxs-lookup"><span data-stu-id="a28b9-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="a28b9-110">參數</span><span class="sxs-lookup"><span data-stu-id="a28b9-110">PARAMETERS</span></span>

### <span data-ttu-id="a28b9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a28b9-111">-DefaultProfile</span></span>
<span data-ttu-id="a28b9-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a28b9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a28b9-113">-KeyName</span><span class="sxs-lookup"><span data-stu-id="a28b9-113">-KeyName</span></span>
<span data-ttu-id="a28b9-114">指定要重新產生的金鑰。</span><span class="sxs-lookup"><span data-stu-id="a28b9-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="a28b9-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a28b9-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a28b9-116">key1</span><span class="sxs-lookup"><span data-stu-id="a28b9-116">key1</span></span>
- <span data-ttu-id="a28b9-117">key2</span><span class="sxs-lookup"><span data-stu-id="a28b9-117">key2</span></span>
- <span data-ttu-id="a28b9-118">kerb1</span><span class="sxs-lookup"><span data-stu-id="a28b9-118">kerb1</span></span>
- <span data-ttu-id="a28b9-119">kerb2</span><span class="sxs-lookup"><span data-stu-id="a28b9-119">kerb2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2, kerb1, kerb2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a28b9-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="a28b9-120">-Name</span></span>
<span data-ttu-id="a28b9-121">指定要重新產生儲存金鑰的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a28b9-121">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="a28b9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a28b9-122">-ResourceGroupName</span></span>
<span data-ttu-id="a28b9-123">指定包含儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a28b9-123">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="a28b9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a28b9-124">CommonParameters</span></span>
<span data-ttu-id="a28b9-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a28b9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a28b9-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a28b9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a28b9-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a28b9-127">INPUTS</span></span>

### <span data-ttu-id="a28b9-128">System.object</span><span class="sxs-lookup"><span data-stu-id="a28b9-128">System.String</span></span>

## <span data-ttu-id="a28b9-129">輸出</span><span class="sxs-lookup"><span data-stu-id="a28b9-129">OUTPUTS</span></span>

### <span data-ttu-id="a28b9-130">StorageAccountListKeysResult （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="a28b9-130">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span></span>

## <span data-ttu-id="a28b9-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a28b9-131">NOTES</span></span>

## <span data-ttu-id="a28b9-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a28b9-132">RELATED LINKS</span></span>

[<span data-ttu-id="a28b9-133">AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a28b9-133">Get-AzStorageAccountKey</span></span>](./Get-AzStorageAccountKey.md)

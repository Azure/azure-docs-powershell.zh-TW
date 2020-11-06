---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
ms.openlocfilehash: e84bb0dd511f5534b8794327b68f2321efcdc130
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445944"
---
# <span data-ttu-id="61d5b-101">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="61d5b-101">Get-AzureRmStorageAccount</span></span>

## <span data-ttu-id="61d5b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="61d5b-102">SYNOPSIS</span></span>
<span data-ttu-id="61d5b-103">取得儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="61d5b-103">Gets a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61d5b-104">句法</span><span class="sxs-lookup"><span data-stu-id="61d5b-104">SYNTAX</span></span>

### <span data-ttu-id="61d5b-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="61d5b-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmStorageAccount [[-ResourceGroupName] <String>] [<CommonParameters>]
```

### <span data-ttu-id="61d5b-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="61d5b-106">AccountNameParameterSet</span></span>
```
Get-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="61d5b-107">說明</span><span class="sxs-lookup"><span data-stu-id="61d5b-107">DESCRIPTION</span></span>
<span data-ttu-id="61d5b-108">**AzureRmStorageAccount** Cmdlet 會取得指定的儲存空間帳戶或資源群組或訂閱中的所有儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="61d5b-108">The **Get-AzureRmStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="61d5b-109">示例</span><span class="sxs-lookup"><span data-stu-id="61d5b-109">EXAMPLES</span></span>

### <span data-ttu-id="61d5b-110">範例1：取得指定的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="61d5b-110">Example 1: Get a specified storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="61d5b-111">這個命令會取得指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="61d5b-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="61d5b-112">範例2：取得資源群組中的所有儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="61d5b-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="61d5b-113">這個命令會取得資源群組中的所有儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="61d5b-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="61d5b-114">範例3：取得訂閱中的所有儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="61d5b-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzureRmStorageAccount
```

<span data-ttu-id="61d5b-115">這個命令會取得訂閱中的所有儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="61d5b-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="61d5b-116">參數</span><span class="sxs-lookup"><span data-stu-id="61d5b-116">PARAMETERS</span></span>

### <span data-ttu-id="61d5b-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="61d5b-117">-Name</span></span>
<span data-ttu-id="61d5b-118">指定要取得的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="61d5b-118">Specifies the name of the Storage account to get.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61d5b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61d5b-119">-ResourceGroupName</span></span>
<span data-ttu-id="61d5b-120">指定包含要取得之儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="61d5b-120">Specifies the name of the resource group that contains the Storage account to get.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61d5b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61d5b-121">CommonParameters</span></span>
<span data-ttu-id="61d5b-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="61d5b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61d5b-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="61d5b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61d5b-124">輸入</span><span class="sxs-lookup"><span data-stu-id="61d5b-124">INPUTS</span></span>

### <span data-ttu-id="61d5b-125">所有</span><span class="sxs-lookup"><span data-stu-id="61d5b-125">None</span></span>
<span data-ttu-id="61d5b-126">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="61d5b-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="61d5b-127">輸出</span><span class="sxs-lookup"><span data-stu-id="61d5b-127">OUTPUTS</span></span>

## <span data-ttu-id="61d5b-128">筆記</span><span class="sxs-lookup"><span data-stu-id="61d5b-128">NOTES</span></span>

## <span data-ttu-id="61d5b-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="61d5b-129">RELATED LINKS</span></span>

[<span data-ttu-id="61d5b-130">新-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="61d5b-130">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="61d5b-131">移除-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="61d5b-131">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="61d5b-132">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="61d5b-132">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)

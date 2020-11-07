---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
ms.openlocfilehash: bf63046ebe8b73f97a80e1465060b6265f99923e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623534"
---
# <span data-ttu-id="ba42f-101">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ba42f-101">Get-AzureRmStorageAccount</span></span>

## <span data-ttu-id="ba42f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ba42f-102">SYNOPSIS</span></span>
<span data-ttu-id="ba42f-103">取得儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="ba42f-103">Gets a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba42f-104">句法</span><span class="sxs-lookup"><span data-stu-id="ba42f-104">SYNTAX</span></span>

### <span data-ttu-id="ba42f-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba42f-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ba42f-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba42f-106">AccountNameParameterSet</span></span>
```
Get-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba42f-107">說明</span><span class="sxs-lookup"><span data-stu-id="ba42f-107">DESCRIPTION</span></span>
<span data-ttu-id="ba42f-108">**AzureRmStorageAccount** Cmdlet 會取得指定的儲存空間帳戶或資源群組或訂閱中的所有儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="ba42f-108">The **Get-AzureRmStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="ba42f-109">示例</span><span class="sxs-lookup"><span data-stu-id="ba42f-109">EXAMPLES</span></span>

### <span data-ttu-id="ba42f-110">範例1：取得指定的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="ba42f-110">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="ba42f-111">這個命令會取得指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="ba42f-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="ba42f-112">範例2：取得資源群組中的所有儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="ba42f-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="ba42f-113">這個命令會取得資源群組中的所有儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="ba42f-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="ba42f-114">範例3：取得訂閱中的所有儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="ba42f-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzureRmStorageAccount
```

<span data-ttu-id="ba42f-115">這個命令會取得訂閱中的所有儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="ba42f-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="ba42f-116">參數</span><span class="sxs-lookup"><span data-stu-id="ba42f-116">PARAMETERS</span></span>

### <span data-ttu-id="ba42f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba42f-117">-DefaultProfile</span></span>
<span data-ttu-id="ba42f-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ba42f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba42f-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="ba42f-119">-Name</span></span>
<span data-ttu-id="ba42f-120">指定要取得的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ba42f-120">Specifies the name of the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba42f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba42f-121">-ResourceGroupName</span></span>
<span data-ttu-id="ba42f-122">指定包含要取得之儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba42f-122">Specifies the name of the resource group that contains the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba42f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba42f-123">CommonParameters</span></span>
<span data-ttu-id="ba42f-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ba42f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba42f-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ba42f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba42f-126">輸入</span><span class="sxs-lookup"><span data-stu-id="ba42f-126">INPUTS</span></span>

### <span data-ttu-id="ba42f-127">System.object</span><span class="sxs-lookup"><span data-stu-id="ba42f-127">System.String</span></span>

## <span data-ttu-id="ba42f-128">輸出</span><span class="sxs-lookup"><span data-stu-id="ba42f-128">OUTPUTS</span></span>

### <span data-ttu-id="ba42f-129">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="ba42f-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="ba42f-130">筆記</span><span class="sxs-lookup"><span data-stu-id="ba42f-130">NOTES</span></span>

## <span data-ttu-id="ba42f-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba42f-131">RELATED LINKS</span></span>

[<span data-ttu-id="ba42f-132">新-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ba42f-132">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="ba42f-133">移除-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ba42f-133">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="ba42f-134">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ba42f-134">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)



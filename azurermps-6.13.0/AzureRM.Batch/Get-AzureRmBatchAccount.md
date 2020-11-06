---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
ms.openlocfilehash: ddc3bab48e766f80375fdf98add15e16e0086fee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445739"
---
# <span data-ttu-id="54aec-101">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="54aec-101">Get-AzureRmBatchAccount</span></span>

## <span data-ttu-id="54aec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="54aec-102">SYNOPSIS</span></span>
<span data-ttu-id="54aec-103">取得目前訂閱中的批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="54aec-103">Gets a Batch account in the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54aec-104">句法</span><span class="sxs-lookup"><span data-stu-id="54aec-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54aec-105">說明</span><span class="sxs-lookup"><span data-stu-id="54aec-105">DESCRIPTION</span></span>
<span data-ttu-id="54aec-106">**AzureRmBatchAccount** Cmdlet 會在目前的訂閱中取得 Azure Batch 帳戶。</span><span class="sxs-lookup"><span data-stu-id="54aec-106">The **Get-AzureRmBatchAccount** cmdlet gets an Azure Batch account in the current subscription.</span></span> <span data-ttu-id="54aec-107">您可以使用 *AccountName* 參數來取得單一帳戶，或者您可以使用 *ResourceGroupName* 參數來取得該資源群組下的帳戶。</span><span class="sxs-lookup"><span data-stu-id="54aec-107">You can use the *AccountName* parameter to get a single account, or you can use the *ResourceGroupName* parameter to get accounts under that resource group.</span></span>

## <span data-ttu-id="54aec-108">示例</span><span class="sxs-lookup"><span data-stu-id="54aec-108">EXAMPLES</span></span>

### <span data-ttu-id="54aec-109">範例1：透過名稱取得批次帳戶</span><span class="sxs-lookup"><span data-stu-id="54aec-109">Example 1: Get a batch account by name</span></span>
```
PS C:\>Get-AzureRmBatchAccount -AccountName "pfuller"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://pfuller.westus.batch.azure.com
```

<span data-ttu-id="54aec-110">這個命令會取得名為 pfuller 的批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="54aec-110">This command gets the batch account named pfuller.</span></span>

### <span data-ttu-id="54aec-111">範例2：取得與資源群組相關聯的批次帳戶</span><span class="sxs-lookup"><span data-stu-id="54aec-111">Example 2: Get the batch accounts associated with a resource group</span></span>
```
PS C:\>Get-AzureRmBatchAccount -ResourceGroupName "CmdletExampleRG"
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
AccountName                  : cmdletexample2
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="54aec-112">這個命令會取得與 CmdletExampleRG 資源群組相關聯的批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="54aec-112">This command gets the batch accounts associated with the CmdletExampleRG resource group.</span></span>

## <span data-ttu-id="54aec-113">參數</span><span class="sxs-lookup"><span data-stu-id="54aec-113">PARAMETERS</span></span>

### <span data-ttu-id="54aec-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="54aec-114">-AccountName</span></span>
<span data-ttu-id="54aec-115">指定帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="54aec-115">Specifies the name of an account.</span></span>
<span data-ttu-id="54aec-116">如果您指定帳戶名稱，這個 Cmdlet 只會傳回該帳戶。</span><span class="sxs-lookup"><span data-stu-id="54aec-116">If you specify an account name, this cmdlet only returns that account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54aec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54aec-117">-DefaultProfile</span></span>
<span data-ttu-id="54aec-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="54aec-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54aec-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54aec-119">-ResourceGroupName</span></span>
<span data-ttu-id="54aec-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="54aec-120">Specifies the name of a resource group.</span></span>
<span data-ttu-id="54aec-121">如果您指定資源群組，此 Cmdlet 會在指定的資源群組下取得帳戶。</span><span class="sxs-lookup"><span data-stu-id="54aec-121">If you specify a resource group, this cmdlet gets the accounts under the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54aec-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="54aec-122">-Tag</span></span>
<span data-ttu-id="54aec-123">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="54aec-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="54aec-124">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"} 這個 Cmdlet 會取得包含此參數所指定之標記的帳戶。</span><span class="sxs-lookup"><span data-stu-id="54aec-124">For example: @{key0="value0";key1=$null;key2="value2"} This cmdlet gets accounts that contain the tags that this parameter specifies.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54aec-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54aec-125">CommonParameters</span></span>
<span data-ttu-id="54aec-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="54aec-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54aec-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="54aec-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54aec-128">輸入</span><span class="sxs-lookup"><span data-stu-id="54aec-128">INPUTS</span></span>

### <span data-ttu-id="54aec-129">System.object</span><span class="sxs-lookup"><span data-stu-id="54aec-129">System.String</span></span>

### <span data-ttu-id="54aec-130">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="54aec-130">System.Collections.Hashtable</span></span>

## <span data-ttu-id="54aec-131">輸出</span><span class="sxs-lookup"><span data-stu-id="54aec-131">OUTPUTS</span></span>

### <span data-ttu-id="54aec-132">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="54aec-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="54aec-133">筆記</span><span class="sxs-lookup"><span data-stu-id="54aec-133">NOTES</span></span>

## <span data-ttu-id="54aec-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="54aec-134">RELATED LINKS</span></span>

[<span data-ttu-id="54aec-135">新-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="54aec-135">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="54aec-136">移除-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="54aec-136">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="54aec-137">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="54aec-137">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="54aec-138">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="54aec-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
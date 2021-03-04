---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9BEE5888-304D-4438-BE97-D1FE254AEE98
online version: https://docs.microsoft.com/powershell/module/az.batch/set-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
ms.openlocfilehash: bbbe4c9b6a9832df490fee1668e953354b0c6d7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909785"
---
# <span data-ttu-id="1172f-101">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="1172f-101">Set-AzBatchAccount</span></span>

## <span data-ttu-id="1172f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1172f-102">SYNOPSIS</span></span>
<span data-ttu-id="1172f-103">更新批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="1172f-103">Updates a Batch account.</span></span>

## <span data-ttu-id="1172f-104">語法</span><span class="sxs-lookup"><span data-stu-id="1172f-104">SYNTAX</span></span>

```
Set-AzBatchAccount [-AccountName] <String> [-Tag] <Hashtable> [-ResourceGroupName <String>]
 [-AutoStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1172f-105">描述</span><span class="sxs-lookup"><span data-stu-id="1172f-105">DESCRIPTION</span></span>
<span data-ttu-id="1172f-106">**Set-AzBatchAccount** Cmdlet 會更新 Azure Batch 帳戶。</span><span class="sxs-lookup"><span data-stu-id="1172f-106">The **Set-AzBatchAccount** cmdlet updates an Azure Batch account.</span></span>
<span data-ttu-id="1172f-107">目前，此 Cmdlet 只能更新標籤。</span><span class="sxs-lookup"><span data-stu-id="1172f-107">Currently, this cmdlet can update only tags.</span></span>

## <span data-ttu-id="1172f-108">例子</span><span class="sxs-lookup"><span data-stu-id="1172f-108">EXAMPLES</span></span>

### <span data-ttu-id="1172f-109">範例 1：更新 Batch 帳戶上的標記</span><span class="sxs-lookup"><span data-stu-id="1172f-109">Example 1: Update the tags on a Batch account</span></span>
```
PS C:\>Set-AzBatchAccount -AccountName "cmdletexample" -Tag @{key0="value0";key1=$null;key2="value2"}
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
                               Name  Value
                               ====  ======
                               key0  value0
                               key1
                               key2  value2
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="1172f-110">此命令會更新名為 pfuller 的帳戶上的標記。</span><span class="sxs-lookup"><span data-stu-id="1172f-110">This command updates the tags on the account named pfuller.</span></span>

## <span data-ttu-id="1172f-111">參數</span><span class="sxs-lookup"><span data-stu-id="1172f-111">PARAMETERS</span></span>

### <span data-ttu-id="1172f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1172f-112">-AccountName</span></span>
<span data-ttu-id="1172f-113">指定此 Cmdlet 更新的批次帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="1172f-113">Specifies the name of the Batch account that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1172f-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1172f-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="1172f-115">指定要用於自動儲存的儲存空間帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1172f-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1172f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1172f-116">-DefaultProfile</span></span>
<span data-ttu-id="1172f-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1172f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1172f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1172f-118">-ResourceGroupName</span></span>
<span data-ttu-id="1172f-119">指定此 Cmdlet 更新之帳戶的資源群組。</span><span class="sxs-lookup"><span data-stu-id="1172f-119">Specifies the resource group of the account that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1172f-120">-標記</span><span class="sxs-lookup"><span data-stu-id="1172f-120">-Tag</span></span>
<span data-ttu-id="1172f-121">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="1172f-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1172f-122">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="1172f-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1172f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1172f-123">CommonParameters</span></span>
<span data-ttu-id="1172f-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1172f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1172f-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1172f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1172f-126">輸入</span><span class="sxs-lookup"><span data-stu-id="1172f-126">INPUTS</span></span>

### <span data-ttu-id="1172f-127">System.String</span><span class="sxs-lookup"><span data-stu-id="1172f-127">System.String</span></span>

### <span data-ttu-id="1172f-128">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1172f-128">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1172f-129">輸出</span><span class="sxs-lookup"><span data-stu-id="1172f-129">OUTPUTS</span></span>

### <span data-ttu-id="1172f-130">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="1172f-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="1172f-131">筆記</span><span class="sxs-lookup"><span data-stu-id="1172f-131">NOTES</span></span>

## <span data-ttu-id="1172f-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="1172f-132">RELATED LINKS</span></span>

[<span data-ttu-id="1172f-133">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="1172f-133">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="1172f-134">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="1172f-134">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="1172f-135">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="1172f-135">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="1172f-136">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1172f-136">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)

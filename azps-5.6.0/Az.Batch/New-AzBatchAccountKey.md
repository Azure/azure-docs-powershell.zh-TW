---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
ms.openlocfilehash: ee5ae846ed83065b797f1389827d7d53ae1988d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917802"
---
# <span data-ttu-id="5899d-101">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="5899d-101">New-AzBatchAccountKey</span></span>

## <span data-ttu-id="5899d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5899d-102">SYNOPSIS</span></span>
<span data-ttu-id="5899d-103">重新產生 Batch 帳戶的金鑰。</span><span class="sxs-lookup"><span data-stu-id="5899d-103">Regenerates a key of a Batch account.</span></span>

## <span data-ttu-id="5899d-104">語法</span><span class="sxs-lookup"><span data-stu-id="5899d-104">SYNTAX</span></span>

```
New-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5899d-105">描述</span><span class="sxs-lookup"><span data-stu-id="5899d-105">DESCRIPTION</span></span>
<span data-ttu-id="5899d-106">**New-AzBatchAccountKey** Cmdlet 會重新產生 Azure Batch 帳戶的主鍵或次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="5899d-106">The **New-AzBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="5899d-107">Cmdlet 會傳回具有其目前 **PrimaryAccountKey** 和 **SecondaryAccountKey** 屬性的 **BatchAccountCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="5899d-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="5899d-108">例子</span><span class="sxs-lookup"><span data-stu-id="5899d-108">EXAMPLES</span></span>

### <span data-ttu-id="5899d-109">範例 1：重新產生 Batch 帳戶的主帳戶金鑰</span><span class="sxs-lookup"><span data-stu-id="5899d-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
```
PS C:\>New-AzBatchAccountKey -AccountName "pfuller" -KeyType "Primary"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="5899d-110">此命令會重新產生 Batch 帳戶上名為 pfuller 的主帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="5899d-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="5899d-111">參數</span><span class="sxs-lookup"><span data-stu-id="5899d-111">PARAMETERS</span></span>

### <span data-ttu-id="5899d-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5899d-112">-AccountName</span></span>
<span data-ttu-id="5899d-113">指定此 Cmdlet 會重新產生金鑰的 Batch 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="5899d-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="5899d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5899d-114">-DefaultProfile</span></span>
<span data-ttu-id="5899d-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5899d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5899d-116">-KeyType</span><span class="sxs-lookup"><span data-stu-id="5899d-116">-KeyType</span></span>
<span data-ttu-id="5899d-117">指定此 Cmdlet 重新產生之金鑰的類型。</span><span class="sxs-lookup"><span data-stu-id="5899d-117">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="5899d-118">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="5899d-118">Valid values are:</span></span>
- <span data-ttu-id="5899d-119">主要</span><span class="sxs-lookup"><span data-stu-id="5899d-119">Primary</span></span>
- <span data-ttu-id="5899d-120">二 次</span><span class="sxs-lookup"><span data-stu-id="5899d-120">Secondary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5899d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5899d-121">-ResourceGroupName</span></span>
<span data-ttu-id="5899d-122">指定此 Cmdlet 重新產生金鑰之帳戶的資源群組。</span><span class="sxs-lookup"><span data-stu-id="5899d-122">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="5899d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5899d-123">CommonParameters</span></span>
<span data-ttu-id="5899d-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5899d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5899d-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5899d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5899d-126">輸入</span><span class="sxs-lookup"><span data-stu-id="5899d-126">INPUTS</span></span>

### <span data-ttu-id="5899d-127">System.String</span><span class="sxs-lookup"><span data-stu-id="5899d-127">System.String</span></span>

## <span data-ttu-id="5899d-128">輸出</span><span class="sxs-lookup"><span data-stu-id="5899d-128">OUTPUTS</span></span>

### <span data-ttu-id="5899d-129">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="5899d-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5899d-130">筆記</span><span class="sxs-lookup"><span data-stu-id="5899d-130">NOTES</span></span>

## <span data-ttu-id="5899d-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="5899d-131">RELATED LINKS</span></span>

[<span data-ttu-id="5899d-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="5899d-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="5899d-133">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5899d-133">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)

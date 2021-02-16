---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
ms.openlocfilehash: 121e4b4b2ffe25d9e5ae53cb03e60cb7a1da91b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141458"
---
# <span data-ttu-id="c5816-101">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="c5816-101">New-AzBatchAccountKey</span></span>

## <span data-ttu-id="c5816-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c5816-102">SYNOPSIS</span></span>
<span data-ttu-id="c5816-103">再生批次帳戶的金鑰。</span><span class="sxs-lookup"><span data-stu-id="c5816-103">Regenerates a key of a Batch account.</span></span>

## <span data-ttu-id="c5816-104">句法</span><span class="sxs-lookup"><span data-stu-id="c5816-104">SYNTAX</span></span>

```
New-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5816-105">說明</span><span class="sxs-lookup"><span data-stu-id="c5816-105">DESCRIPTION</span></span>
<span data-ttu-id="c5816-106">**新的-AzBatchAccountKey** Cmdlet 會重新產生 Azure Batch 帳戶的主要或次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="c5816-106">The **New-AzBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="c5816-107">Cmdlet 會傳回 **BatchAccountCoNtext** 物件，該物件具有其目前的 **PrimaryAccountKey** 和 **SecondaryAccountKey** 屬性。</span><span class="sxs-lookup"><span data-stu-id="c5816-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="c5816-108">示例</span><span class="sxs-lookup"><span data-stu-id="c5816-108">EXAMPLES</span></span>

### <span data-ttu-id="c5816-109">範例1：在批次帳戶上重新產生主要帳戶金鑰</span><span class="sxs-lookup"><span data-stu-id="c5816-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
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

<span data-ttu-id="c5816-110">這個命令會在名為 pfuller 的批次帳戶上，重新生成主要帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="c5816-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="c5816-111">參數</span><span class="sxs-lookup"><span data-stu-id="c5816-111">PARAMETERS</span></span>

### <span data-ttu-id="c5816-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c5816-112">-AccountName</span></span>
<span data-ttu-id="c5816-113">指定此 Cmdlet 為其重新生成金鑰的批次帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="c5816-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="c5816-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5816-114">-DefaultProfile</span></span>
<span data-ttu-id="c5816-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c5816-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5816-116">-KeyType</span><span class="sxs-lookup"><span data-stu-id="c5816-116">-KeyType</span></span>
<span data-ttu-id="c5816-117">指定此 Cmdlet 所再生的金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="c5816-117">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="c5816-118">有效值為：</span><span class="sxs-lookup"><span data-stu-id="c5816-118">Valid values are:</span></span>
- <span data-ttu-id="c5816-119">首選</span><span class="sxs-lookup"><span data-stu-id="c5816-119">Primary</span></span>
- <span data-ttu-id="c5816-120">備用</span><span class="sxs-lookup"><span data-stu-id="c5816-120">Secondary</span></span>

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

### <span data-ttu-id="c5816-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5816-121">-ResourceGroupName</span></span>
<span data-ttu-id="c5816-122">指定此 Cmdlet 為其重新生成金鑰的帳戶資源群組。</span><span class="sxs-lookup"><span data-stu-id="c5816-122">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="c5816-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5816-123">CommonParameters</span></span>
<span data-ttu-id="c5816-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c5816-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5816-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c5816-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5816-126">輸入</span><span class="sxs-lookup"><span data-stu-id="c5816-126">INPUTS</span></span>

### <span data-ttu-id="c5816-127">System.object</span><span class="sxs-lookup"><span data-stu-id="c5816-127">System.String</span></span>

## <span data-ttu-id="c5816-128">輸出</span><span class="sxs-lookup"><span data-stu-id="c5816-128">OUTPUTS</span></span>

### <span data-ttu-id="c5816-129">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="c5816-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c5816-130">筆記</span><span class="sxs-lookup"><span data-stu-id="c5816-130">NOTES</span></span>

## <span data-ttu-id="c5816-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="c5816-131">RELATED LINKS</span></span>

[<span data-ttu-id="c5816-132">AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="c5816-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="c5816-133">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c5816-133">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicycompliancescan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
ms.openlocfilehash: cd173d17b0867fb5c635b77ee6c72847dc845cb7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958913"
---
# <span data-ttu-id="3aaf5-101">Start-AzPolicyComplianceScan</span><span class="sxs-lookup"><span data-stu-id="3aaf5-101">Start-AzPolicyComplianceScan</span></span>

## <span data-ttu-id="3aaf5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3aaf5-102">SYNOPSIS</span></span>
<span data-ttu-id="3aaf5-103">觸發訂閱或資源群組中所有資源的原則合規性評估。</span><span class="sxs-lookup"><span data-stu-id="3aaf5-103">Triggers a policy compliance evaluation for all resources in a subscription or resource group.</span></span>

## <span data-ttu-id="3aaf5-104">句法</span><span class="sxs-lookup"><span data-stu-id="3aaf5-104">SYNTAX</span></span>

```
Start-AzPolicyComplianceScan [-ResourceGroupName <String>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3aaf5-105">說明</span><span class="sxs-lookup"><span data-stu-id="3aaf5-105">DESCRIPTION</span></span>
<span data-ttu-id="3aaf5-106">**AzPolicyComplianceScan** Cmdlet 會啟動訂閱或資源群組的原則合規性評估。</span><span class="sxs-lookup"><span data-stu-id="3aaf5-106">The **Start-AzPolicyComplianceScan** cmdlet starts a policy compliance evaluation for a subscription or resource group.</span></span> <span data-ttu-id="3aaf5-107">該範圍內的所有資源，都會針對所有指派的原則評估其符合性狀態。</span><span class="sxs-lookup"><span data-stu-id="3aaf5-107">All resources within that scope will have their compliance state evaluated against all assigned policies.</span></span>

## <span data-ttu-id="3aaf5-108">示例</span><span class="sxs-lookup"><span data-stu-id="3aaf5-108">EXAMPLES</span></span>

### <span data-ttu-id="3aaf5-109">範例1：在訂閱範圍開始進行合規性掃描</span><span class="sxs-lookup"><span data-stu-id="3aaf5-109">Example 1: Start a compliance scan at subscription scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan
```

<span data-ttu-id="3aaf5-110">這個命令會為使用中的訂閱啟動原則遵從性評估。</span><span class="sxs-lookup"><span data-stu-id="3aaf5-110">This command starts a policy compliance evaluation for the active subscription.</span></span>

### <span data-ttu-id="3aaf5-111">範例2：在資源群組範圍開始進行合規性掃描</span><span class="sxs-lookup"><span data-stu-id="3aaf5-111">Example 2: Start a compliance scan at resource group scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan -ResourceGroupName "myRG"
```

<span data-ttu-id="3aaf5-112">這個命令會針對作用中訂閱中的「myRG」資源群組啟動原則遵從性評估。</span><span class="sxs-lookup"><span data-stu-id="3aaf5-112">This command starts a policy compliance evaluation for the "myRG" resource group in the active subscription.</span></span>

### <span data-ttu-id="3aaf5-113">範例3：啟動合規性掃描並等待其在背景完成</span><span class="sxs-lookup"><span data-stu-id="3aaf5-113">Example 3: Start a compliance scan and wait for it to complete in the background</span></span>
```
PS C:\> $job = Start-AzPolicyComplianceScan
PS C:\> $job | Wait-Job
```

<span data-ttu-id="3aaf5-114">這個命令會為使用中的訂閱啟動原則遵從性評估。</span><span class="sxs-lookup"><span data-stu-id="3aaf5-114">This command starts a policy compliance evaluation for the active subscription.</span></span> <span data-ttu-id="3aaf5-115">它會等到掃描完成。</span><span class="sxs-lookup"><span data-stu-id="3aaf5-115">It will wait for the scan to complete.</span></span>

## <span data-ttu-id="3aaf5-116">參數</span><span class="sxs-lookup"><span data-stu-id="3aaf5-116">PARAMETERS</span></span>

### <span data-ttu-id="3aaf5-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3aaf5-117">-AsJob</span></span>
<span data-ttu-id="3aaf5-118">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3aaf5-118">Run cmdlet in the background.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aaf5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aaf5-119">-DefaultProfile</span></span>
<span data-ttu-id="3aaf5-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3aaf5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aaf5-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3aaf5-121">-PassThru</span></span>
<span data-ttu-id="3aaf5-122">如果命令順利完成，則傳回 True。</span><span class="sxs-lookup"><span data-stu-id="3aaf5-122">Return True if the command completes successfully.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aaf5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3aaf5-123">-ResourceGroupName</span></span>
<span data-ttu-id="3aaf5-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="3aaf5-124">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aaf5-125">-確認</span><span class="sxs-lookup"><span data-stu-id="3aaf5-125">-Confirm</span></span>
<span data-ttu-id="3aaf5-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3aaf5-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aaf5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3aaf5-127">-WhatIf</span></span>
<span data-ttu-id="3aaf5-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3aaf5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3aaf5-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3aaf5-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aaf5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aaf5-130">CommonParameters</span></span>
<span data-ttu-id="3aaf5-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3aaf5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aaf5-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3aaf5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aaf5-133">輸入</span><span class="sxs-lookup"><span data-stu-id="3aaf5-133">INPUTS</span></span>

### <span data-ttu-id="3aaf5-134">System.object</span><span class="sxs-lookup"><span data-stu-id="3aaf5-134">System.String</span></span>

## <span data-ttu-id="3aaf5-135">輸出</span><span class="sxs-lookup"><span data-stu-id="3aaf5-135">OUTPUTS</span></span>

### <span data-ttu-id="3aaf5-136">System.object</span><span class="sxs-lookup"><span data-stu-id="3aaf5-136">System.Boolean</span></span>

## <span data-ttu-id="3aaf5-137">筆記</span><span class="sxs-lookup"><span data-stu-id="3aaf5-137">NOTES</span></span>

## <span data-ttu-id="3aaf5-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="3aaf5-138">RELATED LINKS</span></span>

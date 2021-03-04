---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/start-azpolicycompliancescan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
ms.openlocfilehash: db51cfdf499fcf3d6c81f47d977978a6ff4bf8cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911358"
---
# <span data-ttu-id="24a26-101">Start-AzPolicyComplianceScan</span><span class="sxs-lookup"><span data-stu-id="24a26-101">Start-AzPolicyComplianceScan</span></span>

## <span data-ttu-id="24a26-102">簡介</span><span class="sxs-lookup"><span data-stu-id="24a26-102">SYNOPSIS</span></span>
<span data-ttu-id="24a26-103">觸發訂閱或資源群組中所有資源之策略合規性評估。</span><span class="sxs-lookup"><span data-stu-id="24a26-103">Triggers a policy compliance evaluation for all resources in a subscription or resource group.</span></span>

## <span data-ttu-id="24a26-104">語法</span><span class="sxs-lookup"><span data-stu-id="24a26-104">SYNTAX</span></span>

```
Start-AzPolicyComplianceScan [-ResourceGroupName <String>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24a26-105">描述</span><span class="sxs-lookup"><span data-stu-id="24a26-105">DESCRIPTION</span></span>
<span data-ttu-id="24a26-106">**Start-AzPolicyComplianceScan** Cmdlet 會針對訂閱或資源群組啟動策略合規性評估。</span><span class="sxs-lookup"><span data-stu-id="24a26-106">The **Start-AzPolicyComplianceScan** cmdlet starts a policy compliance evaluation for a subscription or resource group.</span></span> <span data-ttu-id="24a26-107">該範圍內的所有資源都會根據所有已指派之政策評估其合規性狀態。</span><span class="sxs-lookup"><span data-stu-id="24a26-107">All resources within that scope will have their compliance state evaluated against all assigned policies.</span></span>

## <span data-ttu-id="24a26-108">例子</span><span class="sxs-lookup"><span data-stu-id="24a26-108">EXAMPLES</span></span>

### <span data-ttu-id="24a26-109">範例 1：在訂閱範圍中啟動合規性掃描</span><span class="sxs-lookup"><span data-stu-id="24a26-109">Example 1: Start a compliance scan at subscription scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan
```

<span data-ttu-id="24a26-110">此命令會針對使用中訂閱啟動策略合規性評估。</span><span class="sxs-lookup"><span data-stu-id="24a26-110">This command starts a policy compliance evaluation for the active subscription.</span></span>

### <span data-ttu-id="24a26-111">範例 2：在資源群組範圍開始合規性掃描</span><span class="sxs-lookup"><span data-stu-id="24a26-111">Example 2: Start a compliance scan at resource group scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan -ResourceGroupName "myRG"
```

<span data-ttu-id="24a26-112">此命令會針對使用中訂閱中的 "myRG" 資源群組啟動一個策略合規性評估。</span><span class="sxs-lookup"><span data-stu-id="24a26-112">This command starts a policy compliance evaluation for the "myRG" resource group in the active subscription.</span></span>

### <span data-ttu-id="24a26-113">範例 3：開始合規性掃描，並等待它在背景中完成</span><span class="sxs-lookup"><span data-stu-id="24a26-113">Example 3: Start a compliance scan and wait for it to complete in the background</span></span>
```
PS C:\> $job = Start-AzPolicyComplianceScan -AsJob
PS C:\> $job | Wait-Job
```

<span data-ttu-id="24a26-114">此命令會針對使用中訂閱啟動策略合規性評估。</span><span class="sxs-lookup"><span data-stu-id="24a26-114">This command starts a policy compliance evaluation for the active subscription.</span></span> <span data-ttu-id="24a26-115">它會等待掃描完成。</span><span class="sxs-lookup"><span data-stu-id="24a26-115">It will wait for the scan to complete.</span></span>

## <span data-ttu-id="24a26-116">參數</span><span class="sxs-lookup"><span data-stu-id="24a26-116">PARAMETERS</span></span>

### <span data-ttu-id="24a26-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24a26-117">-AsJob</span></span>
<span data-ttu-id="24a26-118">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24a26-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="24a26-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24a26-119">-DefaultProfile</span></span>
<span data-ttu-id="24a26-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="24a26-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24a26-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24a26-121">-PassThru</span></span>
<span data-ttu-id="24a26-122">如果命令成功完成，請返回 True。</span><span class="sxs-lookup"><span data-stu-id="24a26-122">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="24a26-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24a26-123">-ResourceGroupName</span></span>
<span data-ttu-id="24a26-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="24a26-124">Resource group name.</span></span>

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

### <span data-ttu-id="24a26-125">-確認</span><span class="sxs-lookup"><span data-stu-id="24a26-125">-Confirm</span></span>
<span data-ttu-id="24a26-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="24a26-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24a26-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24a26-127">-WhatIf</span></span>
<span data-ttu-id="24a26-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="24a26-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24a26-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24a26-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24a26-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24a26-130">CommonParameters</span></span>
<span data-ttu-id="24a26-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="24a26-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24a26-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24a26-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24a26-133">輸入</span><span class="sxs-lookup"><span data-stu-id="24a26-133">INPUTS</span></span>

### <span data-ttu-id="24a26-134">System.String</span><span class="sxs-lookup"><span data-stu-id="24a26-134">System.String</span></span>

## <span data-ttu-id="24a26-135">輸出</span><span class="sxs-lookup"><span data-stu-id="24a26-135">OUTPUTS</span></span>

### <span data-ttu-id="24a26-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="24a26-136">System.Boolean</span></span>

## <span data-ttu-id="24a26-137">筆記</span><span class="sxs-lookup"><span data-stu-id="24a26-137">NOTES</span></span>

## <span data-ttu-id="24a26-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="24a26-138">RELATED LINKS</span></span>

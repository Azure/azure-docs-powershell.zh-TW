---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 556cc10b415b2e37b832f144a01d307a2b69e52d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136411"
---
# <span data-ttu-id="6cf14-101">Remove-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="6cf14-101">Remove-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="6cf14-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6cf14-102">SYNOPSIS</span></span>
<span data-ttu-id="6cf14-103">移除指定的 Azure Data Lake Analytics 計算原則</span><span class="sxs-lookup"><span data-stu-id="6cf14-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

## <span data-ttu-id="6cf14-104">句法</span><span class="sxs-lookup"><span data-stu-id="6cf14-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cf14-105">說明</span><span class="sxs-lookup"><span data-stu-id="6cf14-105">DESCRIPTION</span></span>
<span data-ttu-id="6cf14-106">**移除-AzDataLakeAnalyticsComputePolicy** 會移除指定的 Azure Data Lake Analytics 計算原則。</span><span class="sxs-lookup"><span data-stu-id="6cf14-106">The **Remove-AzDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="6cf14-107">示例</span><span class="sxs-lookup"><span data-stu-id="6cf14-107">EXAMPLES</span></span>

### <span data-ttu-id="6cf14-108">範例1：移除計算原則</span><span class="sxs-lookup"><span data-stu-id="6cf14-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="6cf14-109">此命令會移除帳戶 "contosoadla" 中名為 "myPolicy" 的指定計算原則。</span><span class="sxs-lookup"><span data-stu-id="6cf14-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="6cf14-110">參數</span><span class="sxs-lookup"><span data-stu-id="6cf14-110">PARAMETERS</span></span>

### <span data-ttu-id="6cf14-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="6cf14-111">-Account</span></span>
<span data-ttu-id="6cf14-112">要移除其計算原則的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="6cf14-112">Name of the account to remove the compute policy from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cf14-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cf14-113">-DefaultProfile</span></span>
<span data-ttu-id="6cf14-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6cf14-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6cf14-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="6cf14-115">-Name</span></span>
<span data-ttu-id="6cf14-116">要移除之計算原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="6cf14-116">Name of the compute policy to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cf14-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6cf14-117">-PassThru</span></span>
<span data-ttu-id="6cf14-118">成功刪除時，傳回 true。</span><span class="sxs-lookup"><span data-stu-id="6cf14-118">Return true upon successful deletion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cf14-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cf14-119">-ResourceGroupName</span></span>
<span data-ttu-id="6cf14-120">您帳戶所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6cf14-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="6cf14-121">[選用]，如果未提供，就會嘗試探索。</span><span class="sxs-lookup"><span data-stu-id="6cf14-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="6cf14-122">-確認</span><span class="sxs-lookup"><span data-stu-id="6cf14-122">-Confirm</span></span>
<span data-ttu-id="6cf14-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6cf14-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cf14-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cf14-124">-WhatIf</span></span>
<span data-ttu-id="6cf14-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6cf14-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cf14-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6cf14-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cf14-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cf14-127">CommonParameters</span></span>
<span data-ttu-id="6cf14-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6cf14-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cf14-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6cf14-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cf14-130">輸入</span><span class="sxs-lookup"><span data-stu-id="6cf14-130">INPUTS</span></span>

### <span data-ttu-id="6cf14-131">System.object</span><span class="sxs-lookup"><span data-stu-id="6cf14-131">System.String</span></span>

## <span data-ttu-id="6cf14-132">輸出</span><span class="sxs-lookup"><span data-stu-id="6cf14-132">OUTPUTS</span></span>

### <span data-ttu-id="6cf14-133">System.object</span><span class="sxs-lookup"><span data-stu-id="6cf14-133">System.Boolean</span></span>

## <span data-ttu-id="6cf14-134">筆記</span><span class="sxs-lookup"><span data-stu-id="6cf14-134">NOTES</span></span>

## <span data-ttu-id="6cf14-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="6cf14-135">RELATED LINKS</span></span>

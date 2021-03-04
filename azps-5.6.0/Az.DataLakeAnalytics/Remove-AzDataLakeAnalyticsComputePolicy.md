---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 1e6f6957adc8a67e1d92c0aad6f2be035b4f390d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904702"
---
# <span data-ttu-id="9996e-101">Remove-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="9996e-101">Remove-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="9996e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9996e-102">SYNOPSIS</span></span>
<span data-ttu-id="9996e-103">移除指定的 Azure Data Lake Analytics 計算策略</span><span class="sxs-lookup"><span data-stu-id="9996e-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

## <span data-ttu-id="9996e-104">語法</span><span class="sxs-lookup"><span data-stu-id="9996e-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9996e-105">描述</span><span class="sxs-lookup"><span data-stu-id="9996e-105">DESCRIPTION</span></span>
<span data-ttu-id="9996e-106">**Remove-AzDataLakeAnalyticsComputePolicy** 會移除指定的 Azure Data Lake Analytics 計算策略。</span><span class="sxs-lookup"><span data-stu-id="9996e-106">The **Remove-AzDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="9996e-107">例子</span><span class="sxs-lookup"><span data-stu-id="9996e-107">EXAMPLES</span></span>

### <span data-ttu-id="9996e-108">範例 1：移除計算策略</span><span class="sxs-lookup"><span data-stu-id="9996e-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="9996e-109">此命令會移除帳戶 'contodla' 中名稱為 "myPolicy" 的指定計算策略。</span><span class="sxs-lookup"><span data-stu-id="9996e-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="9996e-110">參數</span><span class="sxs-lookup"><span data-stu-id="9996e-110">PARAMETERS</span></span>

### <span data-ttu-id="9996e-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="9996e-111">-Account</span></span>
<span data-ttu-id="9996e-112">要從移除計算策略的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="9996e-112">Name of the account to remove the compute policy from.</span></span>

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

### <span data-ttu-id="9996e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9996e-113">-DefaultProfile</span></span>
<span data-ttu-id="9996e-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="9996e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9996e-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="9996e-115">-Name</span></span>
<span data-ttu-id="9996e-116">要移除的計算策略名稱。</span><span class="sxs-lookup"><span data-stu-id="9996e-116">Name of the compute policy to remove.</span></span>

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

### <span data-ttu-id="9996e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9996e-117">-PassThru</span></span>
<span data-ttu-id="9996e-118">成功刪除時，再返回 True。</span><span class="sxs-lookup"><span data-stu-id="9996e-118">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="9996e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9996e-119">-ResourceGroupName</span></span>
<span data-ttu-id="9996e-120">您帳戶存在下的資源組名。</span><span class="sxs-lookup"><span data-stu-id="9996e-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="9996e-121">選擇性，並嘗試探索是否未提供。</span><span class="sxs-lookup"><span data-stu-id="9996e-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="9996e-122">-確認</span><span class="sxs-lookup"><span data-stu-id="9996e-122">-Confirm</span></span>
<span data-ttu-id="9996e-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9996e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9996e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9996e-124">-WhatIf</span></span>
<span data-ttu-id="9996e-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9996e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9996e-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9996e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9996e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9996e-127">CommonParameters</span></span>
<span data-ttu-id="9996e-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9996e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9996e-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="9996e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9996e-130">輸入</span><span class="sxs-lookup"><span data-stu-id="9996e-130">INPUTS</span></span>

### <span data-ttu-id="9996e-131">System.String</span><span class="sxs-lookup"><span data-stu-id="9996e-131">System.String</span></span>

## <span data-ttu-id="9996e-132">輸出</span><span class="sxs-lookup"><span data-stu-id="9996e-132">OUTPUTS</span></span>

### <span data-ttu-id="9996e-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9996e-133">System.Boolean</span></span>

## <span data-ttu-id="9996e-134">筆記</span><span class="sxs-lookup"><span data-stu-id="9996e-134">NOTES</span></span>

## <span data-ttu-id="9996e-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="9996e-135">RELATED LINKS</span></span>

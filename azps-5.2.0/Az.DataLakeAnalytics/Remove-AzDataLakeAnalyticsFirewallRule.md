---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 879897b6d89e5a1e34ee9f61714628aa741a670f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279176"
---
# <span data-ttu-id="2335e-101">Remove-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2335e-101">Remove-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="2335e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2335e-102">SYNOPSIS</span></span>
<span data-ttu-id="2335e-103">從 Data Lake Analytics 帳戶移除防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="2335e-103">Removes a firewall rule from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="2335e-104">句法</span><span class="sxs-lookup"><span data-stu-id="2335e-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2335e-105">說明</span><span class="sxs-lookup"><span data-stu-id="2335e-105">DESCRIPTION</span></span>
<span data-ttu-id="2335e-106">**AzDataLakeAnalyticsFirewallRule** Cmdlet 會從 Azure Data Lake Analytics 帳戶中移除防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="2335e-106">The **Remove-AzDataLakeAnalyticsFirewallRule** cmdlet removes a firewall rule from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="2335e-107">示例</span><span class="sxs-lookup"><span data-stu-id="2335e-107">EXAMPLES</span></span>

### <span data-ttu-id="2335e-108">範例1：移除防火牆規則</span><span class="sxs-lookup"><span data-stu-id="2335e-108">Example 1: Remove a firewall rule</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="2335e-109">這個命令會從帳戶 "ContosoAdlAcct" 移除名為「我的防火牆規則」的防火牆規則</span><span class="sxs-lookup"><span data-stu-id="2335e-109">This command removes the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="2335e-110">參數</span><span class="sxs-lookup"><span data-stu-id="2335e-110">PARAMETERS</span></span>

### <span data-ttu-id="2335e-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="2335e-111">-Account</span></span>
<span data-ttu-id="2335e-112">要從中移除防火牆規則的資料 Lake Analytics 帳戶</span><span class="sxs-lookup"><span data-stu-id="2335e-112">The Data Lake Analytics account to remove the firewall rule from</span></span>

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

### <span data-ttu-id="2335e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2335e-113">-DefaultProfile</span></span>
<span data-ttu-id="2335e-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2335e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2335e-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="2335e-115">-Name</span></span>
<span data-ttu-id="2335e-116">防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="2335e-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="2335e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2335e-117">-PassThru</span></span>
<span data-ttu-id="2335e-118">表示應傳回指示刪除操作結果的布林回應。</span><span class="sxs-lookup"><span data-stu-id="2335e-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2335e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2335e-119">-ResourceGroupName</span></span>
<span data-ttu-id="2335e-120">要在其下檢索帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2335e-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="2335e-121">-確認</span><span class="sxs-lookup"><span data-stu-id="2335e-121">-Confirm</span></span>
<span data-ttu-id="2335e-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2335e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2335e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2335e-123">-WhatIf</span></span>
<span data-ttu-id="2335e-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2335e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2335e-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2335e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2335e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2335e-126">CommonParameters</span></span>
<span data-ttu-id="2335e-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2335e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2335e-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2335e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2335e-129">輸入</span><span class="sxs-lookup"><span data-stu-id="2335e-129">INPUTS</span></span>

### <span data-ttu-id="2335e-130">System.object</span><span class="sxs-lookup"><span data-stu-id="2335e-130">System.String</span></span>

### <span data-ttu-id="2335e-131">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="2335e-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2335e-132">輸出</span><span class="sxs-lookup"><span data-stu-id="2335e-132">OUTPUTS</span></span>

### <span data-ttu-id="2335e-133">System.object</span><span class="sxs-lookup"><span data-stu-id="2335e-133">System.Boolean</span></span>

## <span data-ttu-id="2335e-134">筆記</span><span class="sxs-lookup"><span data-stu-id="2335e-134">NOTES</span></span>

## <span data-ttu-id="2335e-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="2335e-135">RELATED LINKS</span></span>

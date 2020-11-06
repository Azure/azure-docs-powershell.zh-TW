---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 239e9325532b18140a36e4b8f9a8f291e508a91c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447374"
---
# <span data-ttu-id="188c3-101">Remove-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="188c3-101">Remove-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="188c3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="188c3-102">SYNOPSIS</span></span>
<span data-ttu-id="188c3-103">從 Data Lake Analytics 帳戶移除防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="188c3-103">Removes a firewall rule from a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="188c3-104">句法</span><span class="sxs-lookup"><span data-stu-id="188c3-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="188c3-105">說明</span><span class="sxs-lookup"><span data-stu-id="188c3-105">DESCRIPTION</span></span>
<span data-ttu-id="188c3-106">**AzureRmDataLakeAnalyticsFirewallRule** Cmdlet 會從 Azure Data Lake Analytics 帳戶中移除防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="188c3-106">The **Remove-AzureRmDataLakeAnalyticsFirewallRule** cmdlet removes a firewall rule from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="188c3-107">示例</span><span class="sxs-lookup"><span data-stu-id="188c3-107">EXAMPLES</span></span>

### <span data-ttu-id="188c3-108">範例1：移除防火牆規則</span><span class="sxs-lookup"><span data-stu-id="188c3-108">Example 1: Remove a firewall rule</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="188c3-109">這個命令會從帳戶 "ContosoAdlAcct" 移除名為「我的防火牆規則」的防火牆規則</span><span class="sxs-lookup"><span data-stu-id="188c3-109">This command removes the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="188c3-110">參數</span><span class="sxs-lookup"><span data-stu-id="188c3-110">PARAMETERS</span></span>

### <span data-ttu-id="188c3-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="188c3-111">-Account</span></span>
<span data-ttu-id="188c3-112">要從中移除防火牆規則的資料 Lake Analytics 帳戶</span><span class="sxs-lookup"><span data-stu-id="188c3-112">The Data Lake Analytics account to remove the firewall rule from</span></span>

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

### <span data-ttu-id="188c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="188c3-113">-DefaultProfile</span></span>
<span data-ttu-id="188c3-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="188c3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="188c3-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="188c3-115">-Name</span></span>
<span data-ttu-id="188c3-116">防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="188c3-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="188c3-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="188c3-117">-PassThru</span></span>
<span data-ttu-id="188c3-118">表示應傳回指示刪除操作結果的布林回應。</span><span class="sxs-lookup"><span data-stu-id="188c3-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="188c3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="188c3-119">-ResourceGroupName</span></span>
<span data-ttu-id="188c3-120">要在其下檢索帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="188c3-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="188c3-121">-確認</span><span class="sxs-lookup"><span data-stu-id="188c3-121">-Confirm</span></span>
<span data-ttu-id="188c3-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="188c3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="188c3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="188c3-123">-WhatIf</span></span>
<span data-ttu-id="188c3-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="188c3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="188c3-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="188c3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="188c3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="188c3-126">CommonParameters</span></span>
<span data-ttu-id="188c3-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="188c3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="188c3-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="188c3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="188c3-129">輸入</span><span class="sxs-lookup"><span data-stu-id="188c3-129">INPUTS</span></span>

### <span data-ttu-id="188c3-130">System.object</span><span class="sxs-lookup"><span data-stu-id="188c3-130">System.String</span></span>

### <span data-ttu-id="188c3-131">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="188c3-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="188c3-132">輸出</span><span class="sxs-lookup"><span data-stu-id="188c3-132">OUTPUTS</span></span>

### <span data-ttu-id="188c3-133">System.object</span><span class="sxs-lookup"><span data-stu-id="188c3-133">System.Boolean</span></span>

## <span data-ttu-id="188c3-134">筆記</span><span class="sxs-lookup"><span data-stu-id="188c3-134">NOTES</span></span>

## <span data-ttu-id="188c3-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="188c3-135">RELATED LINKS</span></span>

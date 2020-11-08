---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 91941fbef7363a56da8a8021294750cc862aab55
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136476"
---
# <span data-ttu-id="0fe78-101">Set-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0fe78-101">Set-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="0fe78-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0fe78-102">SYNOPSIS</span></span>
<span data-ttu-id="0fe78-103">更新 Data Lake Analytics 帳戶中的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="0fe78-103">Updates a firewall rule in a Data Lake Analytics account.</span></span>

## <span data-ttu-id="0fe78-104">句法</span><span class="sxs-lookup"><span data-stu-id="0fe78-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fe78-105">說明</span><span class="sxs-lookup"><span data-stu-id="0fe78-105">DESCRIPTION</span></span>
<span data-ttu-id="0fe78-106">**AzDataLakeAnalyticsFirewallRule** Cmdlet 會更新 Azure Data Lake Analytics 帳戶中的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="0fe78-106">The **Set-AzDataLakeAnalyticsFirewallRule** cmdlet updates a firewall rule in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="0fe78-107">示例</span><span class="sxs-lookup"><span data-stu-id="0fe78-107">EXAMPLES</span></span>

### <span data-ttu-id="0fe78-108">範例1：更新防火牆規則</span><span class="sxs-lookup"><span data-stu-id="0fe78-108">Example 1: Update a firewall rule</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="0fe78-109">這個命令會更新帳戶 "ContosoAdlAcct" 中名為「我的防火牆規則」的防火牆規則，讓新的 IP 範圍： 127.0.0.1-127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="0fe78-109">This command updates the firewall rule named "my firewall rule" in account "ContosoAdlAcct" to have the new IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="0fe78-110">參數</span><span class="sxs-lookup"><span data-stu-id="0fe78-110">PARAMETERS</span></span>

### <span data-ttu-id="0fe78-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="0fe78-111">-Account</span></span>
<span data-ttu-id="0fe78-112">要在其中更新防火牆規則的 Data Lake Analytics 帳戶</span><span class="sxs-lookup"><span data-stu-id="0fe78-112">The Data Lake Analytics account to update the firewall rule in</span></span>

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

### <span data-ttu-id="0fe78-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fe78-113">-DefaultProfile</span></span>
<span data-ttu-id="0fe78-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0fe78-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0fe78-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="0fe78-115">-EndIpAddress</span></span>
<span data-ttu-id="0fe78-116">防火牆規則有效 ip 範圍的結尾</span><span class="sxs-lookup"><span data-stu-id="0fe78-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe78-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="0fe78-117">-Name</span></span>
<span data-ttu-id="0fe78-118">防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="0fe78-118">The name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe78-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fe78-119">-ResourceGroupName</span></span>
<span data-ttu-id="0fe78-120">要在其下檢索帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0fe78-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="0fe78-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="0fe78-121">-StartIpAddress</span></span>
<span data-ttu-id="0fe78-122">防火牆規則的有效 ip 範圍起點</span><span class="sxs-lookup"><span data-stu-id="0fe78-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe78-123">-確認</span><span class="sxs-lookup"><span data-stu-id="0fe78-123">-Confirm</span></span>
<span data-ttu-id="0fe78-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0fe78-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fe78-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fe78-125">-WhatIf</span></span>
<span data-ttu-id="0fe78-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0fe78-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fe78-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0fe78-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fe78-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fe78-128">CommonParameters</span></span>
<span data-ttu-id="0fe78-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0fe78-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fe78-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0fe78-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fe78-131">輸入</span><span class="sxs-lookup"><span data-stu-id="0fe78-131">INPUTS</span></span>

### <span data-ttu-id="0fe78-132">System.object</span><span class="sxs-lookup"><span data-stu-id="0fe78-132">System.String</span></span>

## <span data-ttu-id="0fe78-133">輸出</span><span class="sxs-lookup"><span data-stu-id="0fe78-133">OUTPUTS</span></span>

### <span data-ttu-id="0fe78-134">DataLakeAnalyticsFirewallRule 中的 DataLakeAnalytics。</span><span class="sxs-lookup"><span data-stu-id="0fe78-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="0fe78-135">筆記</span><span class="sxs-lookup"><span data-stu-id="0fe78-135">NOTES</span></span>

## <span data-ttu-id="0fe78-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="0fe78-136">RELATED LINKS</span></span>
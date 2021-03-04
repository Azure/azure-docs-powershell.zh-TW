---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/add-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: ed5d4514603ccefeefa4e99d9458434ffeb17cba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905121"
---
# <span data-ttu-id="605e3-101">Add-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="605e3-101">Add-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="605e3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="605e3-102">SYNOPSIS</span></span>
<span data-ttu-id="605e3-103">新增防火牆規則至 Data Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="605e3-103">Adds a firewall rule to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="605e3-104">語法</span><span class="sxs-lookup"><span data-stu-id="605e3-104">SYNTAX</span></span>

```
Add-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="605e3-105">描述</span><span class="sxs-lookup"><span data-stu-id="605e3-105">DESCRIPTION</span></span>
<span data-ttu-id="605e3-106">**Add-AzDataLakeAnalyticsFirewallRule** Cmdlet 會新增防火牆規則至 Azure Data Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="605e3-106">The **Add-AzDataLakeAnalyticsFirewallRule** cmdlet adds a firewall rule to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="605e3-107">例子</span><span class="sxs-lookup"><span data-stu-id="605e3-107">EXAMPLES</span></span>

### <span data-ttu-id="605e3-108">範例 1：新增防火牆規則</span><span class="sxs-lookup"><span data-stu-id="605e3-108">Example 1: Add a firewall rule</span></span>
```
PS C:\>Add-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="605e3-109">此命令會將帳戶"ContosoAdlAcct"的防火牆規則與 IP 範圍：127.0.0.1 - 127.0.0.10 相加，</span><span class="sxs-lookup"><span data-stu-id="605e3-109">This command adds the firewall rule named "my firewall rule" from account "ContosoAdlAcct" with the IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="605e3-110">參數</span><span class="sxs-lookup"><span data-stu-id="605e3-110">PARAMETERS</span></span>

### <span data-ttu-id="605e3-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="605e3-111">-Account</span></span>
<span data-ttu-id="605e3-112">資料湖分析帳戶以新增防火牆規則至</span><span class="sxs-lookup"><span data-stu-id="605e3-112">The Data Lake Analytics account to add the firewall rule to</span></span>

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

### <span data-ttu-id="605e3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="605e3-113">-DefaultProfile</span></span>
<span data-ttu-id="605e3-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="605e3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="605e3-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="605e3-115">-EndIpAddress</span></span>
<span data-ttu-id="605e3-116">防火牆規則的有效 ip 範圍結尾</span><span class="sxs-lookup"><span data-stu-id="605e3-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="605e3-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="605e3-117">-Name</span></span>
<span data-ttu-id="605e3-118">防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="605e3-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="605e3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="605e3-119">-ResourceGroupName</span></span>
<span data-ttu-id="605e3-120">要用於取回帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="605e3-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="605e3-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="605e3-121">-StartIpAddress</span></span>
<span data-ttu-id="605e3-122">防火牆規則的有效 ip 範圍的開始</span><span class="sxs-lookup"><span data-stu-id="605e3-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="605e3-123">-確認</span><span class="sxs-lookup"><span data-stu-id="605e3-123">-Confirm</span></span>
<span data-ttu-id="605e3-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="605e3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="605e3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="605e3-125">-WhatIf</span></span>
<span data-ttu-id="605e3-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="605e3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="605e3-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="605e3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="605e3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="605e3-128">CommonParameters</span></span>
<span data-ttu-id="605e3-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="605e3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="605e3-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="605e3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="605e3-131">輸入</span><span class="sxs-lookup"><span data-stu-id="605e3-131">INPUTS</span></span>

### <span data-ttu-id="605e3-132">System.String</span><span class="sxs-lookup"><span data-stu-id="605e3-132">System.String</span></span>

## <span data-ttu-id="605e3-133">輸出</span><span class="sxs-lookup"><span data-stu-id="605e3-133">OUTPUTS</span></span>

### <span data-ttu-id="605e3-134">Microsoft.Azure.Commands.DataLakeAnalytics.models.DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="605e3-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="605e3-135">筆記</span><span class="sxs-lookup"><span data-stu-id="605e3-135">NOTES</span></span>

## <span data-ttu-id="605e3-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="605e3-136">RELATED LINKS</span></span>

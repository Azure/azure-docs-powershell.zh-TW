---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 9fbb2064a7b7869af450ad267f73c6dc2e2b9a9a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916755"
---
# <span data-ttu-id="f8426-101">Set-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f8426-101">Set-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="f8426-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f8426-102">SYNOPSIS</span></span>
<span data-ttu-id="f8426-103">更新 Data Lake Analytics 帳戶中的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="f8426-103">Updates a firewall rule in a Data Lake Analytics account.</span></span>

## <span data-ttu-id="f8426-104">語法</span><span class="sxs-lookup"><span data-stu-id="f8426-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8426-105">描述</span><span class="sxs-lookup"><span data-stu-id="f8426-105">DESCRIPTION</span></span>
<span data-ttu-id="f8426-106">**Set-AzDataLakeAnalyticsFirewallRule** Cmdlet 會更新 Azure Data Lake Analytics 帳戶中的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="f8426-106">The **Set-AzDataLakeAnalyticsFirewallRule** cmdlet updates a firewall rule in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="f8426-107">例子</span><span class="sxs-lookup"><span data-stu-id="f8426-107">EXAMPLES</span></span>

### <span data-ttu-id="f8426-108">範例 1：更新防火牆規則</span><span class="sxs-lookup"><span data-stu-id="f8426-108">Example 1: Update a firewall rule</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="f8426-109">此命令會更新帳戶 "ContosoAdlAcct" 中名為「我的防火牆規則」的防火牆規則，以擁有新的 IP 範圍：127.0.0.1 - 127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="f8426-109">This command updates the firewall rule named "my firewall rule" in account "ContosoAdlAcct" to have the new IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="f8426-110">參數</span><span class="sxs-lookup"><span data-stu-id="f8426-110">PARAMETERS</span></span>

### <span data-ttu-id="f8426-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="f8426-111">-Account</span></span>
<span data-ttu-id="f8426-112">Data Lake Analytics 帳戶更新</span><span class="sxs-lookup"><span data-stu-id="f8426-112">The Data Lake Analytics account to update the firewall rule in</span></span>

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

### <span data-ttu-id="f8426-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8426-113">-DefaultProfile</span></span>
<span data-ttu-id="f8426-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="f8426-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8426-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="f8426-115">-EndIpAddress</span></span>
<span data-ttu-id="f8426-116">防火牆規則的有效 ip 範圍結尾</span><span class="sxs-lookup"><span data-stu-id="f8426-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="f8426-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="f8426-117">-Name</span></span>
<span data-ttu-id="f8426-118">防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8426-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="f8426-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8426-119">-ResourceGroupName</span></span>
<span data-ttu-id="f8426-120">要用於取回帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f8426-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="f8426-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="f8426-121">-StartIpAddress</span></span>
<span data-ttu-id="f8426-122">防火牆規則的有效 ip 範圍的開始</span><span class="sxs-lookup"><span data-stu-id="f8426-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="f8426-123">-確認</span><span class="sxs-lookup"><span data-stu-id="f8426-123">-Confirm</span></span>
<span data-ttu-id="f8426-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f8426-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8426-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8426-125">-WhatIf</span></span>
<span data-ttu-id="f8426-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f8426-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8426-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f8426-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8426-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8426-128">CommonParameters</span></span>
<span data-ttu-id="f8426-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f8426-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8426-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f8426-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8426-131">輸入</span><span class="sxs-lookup"><span data-stu-id="f8426-131">INPUTS</span></span>

### <span data-ttu-id="f8426-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f8426-132">System.String</span></span>

## <span data-ttu-id="f8426-133">輸出</span><span class="sxs-lookup"><span data-stu-id="f8426-133">OUTPUTS</span></span>

### <span data-ttu-id="f8426-134">Microsoft.Azure.Commands.DataLakeAnalytics.models.DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f8426-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="f8426-135">筆記</span><span class="sxs-lookup"><span data-stu-id="f8426-135">NOTES</span></span>

## <span data-ttu-id="f8426-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8426-136">RELATED LINKS</span></span>

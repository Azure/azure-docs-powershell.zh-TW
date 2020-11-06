---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 98ebcd2380cf20d9fbe12d9538f112c8efca5335
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448693"
---
# <span data-ttu-id="2da48-101">Set-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2da48-101">Set-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="2da48-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2da48-102">SYNOPSIS</span></span>
<span data-ttu-id="2da48-103">更新 Data Lake Analytics 帳戶中的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="2da48-103">Updates a firewall rule in a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2da48-104">句法</span><span class="sxs-lookup"><span data-stu-id="2da48-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2da48-105">說明</span><span class="sxs-lookup"><span data-stu-id="2da48-105">DESCRIPTION</span></span>
<span data-ttu-id="2da48-106">**AzureRmDataLakeAnalyticsFirewallRule** Cmdlet 會更新 Azure Data Lake Analytics 帳戶中的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="2da48-106">The **Set-AzureRmDataLakeAnalyticsFirewallRule** cmdlet updates a firewall rule in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="2da48-107">示例</span><span class="sxs-lookup"><span data-stu-id="2da48-107">EXAMPLES</span></span>

### <span data-ttu-id="2da48-108">範例1：更新防火牆規則</span><span class="sxs-lookup"><span data-stu-id="2da48-108">Example 1: Update a firewall rule</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="2da48-109">這個命令會更新帳戶 "ContosoAdlAcct" 中名為「我的防火牆規則」的防火牆規則，讓新的 IP 範圍： 127.0.0.1-127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="2da48-109">This command updates the firewall rule named "my firewall rule" in account "ContosoAdlAcct" to have the new IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="2da48-110">參數</span><span class="sxs-lookup"><span data-stu-id="2da48-110">PARAMETERS</span></span>

### <span data-ttu-id="2da48-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="2da48-111">-Account</span></span>
<span data-ttu-id="2da48-112">要在其中更新防火牆規則的 Data Lake Analytics 帳戶</span><span class="sxs-lookup"><span data-stu-id="2da48-112">The Data Lake Analytics account to update the firewall rule in</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2da48-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2da48-113">-DefaultProfile</span></span>
<span data-ttu-id="2da48-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2da48-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2da48-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="2da48-115">-EndIpAddress</span></span>
<span data-ttu-id="2da48-116">防火牆規則有效 ip 範圍的結尾</span><span class="sxs-lookup"><span data-stu-id="2da48-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2da48-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="2da48-117">-Name</span></span>
<span data-ttu-id="2da48-118">防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="2da48-118">The name of the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2da48-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2da48-119">-ResourceGroupName</span></span>
<span data-ttu-id="2da48-120">要在其下檢索帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2da48-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="2da48-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="2da48-121">-StartIpAddress</span></span>
<span data-ttu-id="2da48-122">防火牆規則的有效 ip 範圍起點</span><span class="sxs-lookup"><span data-stu-id="2da48-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2da48-123">-確認</span><span class="sxs-lookup"><span data-stu-id="2da48-123">-Confirm</span></span>
<span data-ttu-id="2da48-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2da48-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2da48-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2da48-125">-WhatIf</span></span>
<span data-ttu-id="2da48-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2da48-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2da48-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2da48-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2da48-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2da48-128">CommonParameters</span></span>
<span data-ttu-id="2da48-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2da48-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2da48-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2da48-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2da48-131">輸入</span><span class="sxs-lookup"><span data-stu-id="2da48-131">INPUTS</span></span>

### <span data-ttu-id="2da48-132">System.object</span><span class="sxs-lookup"><span data-stu-id="2da48-132">System.String</span></span>

## <span data-ttu-id="2da48-133">輸出</span><span class="sxs-lookup"><span data-stu-id="2da48-133">OUTPUTS</span></span>

### <span data-ttu-id="2da48-134">DataLakeAnalyticsFirewallRule 中的 DataLakeAnalytics。</span><span class="sxs-lookup"><span data-stu-id="2da48-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="2da48-135">筆記</span><span class="sxs-lookup"><span data-stu-id="2da48-135">NOTES</span></span>

## <span data-ttu-id="2da48-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="2da48-136">RELATED LINKS</span></span>


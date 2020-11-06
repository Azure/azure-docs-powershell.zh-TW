---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 585e0cd6a3cd74c8077833f6b5599b076c2a5db6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446844"
---
# <span data-ttu-id="c9a30-101">Add-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c9a30-101">Add-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="c9a30-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c9a30-102">SYNOPSIS</span></span>
<span data-ttu-id="c9a30-103">在 Data Lake Analytics 帳戶中新增防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="c9a30-103">Adds a firewall rule to a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9a30-104">句法</span><span class="sxs-lookup"><span data-stu-id="c9a30-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9a30-105">說明</span><span class="sxs-lookup"><span data-stu-id="c9a30-105">DESCRIPTION</span></span>
<span data-ttu-id="c9a30-106">**載入 AzureRmDataLakeAnalyticsFirewallRule** Cmdlet 會將防火牆規則新增至 Azure Data Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="c9a30-106">The **Add-AzureRmDataLakeAnalyticsFirewallRule** cmdlet adds a firewall rule to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="c9a30-107">示例</span><span class="sxs-lookup"><span data-stu-id="c9a30-107">EXAMPLES</span></span>

### <span data-ttu-id="c9a30-108">範例1：新增防火牆規則</span><span class="sxs-lookup"><span data-stu-id="c9a30-108">Example 1: Add a firewall rule</span></span>
```
PS C:\>Add-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="c9a30-109">這個命令會將名為「我的防火牆規則」的防火牆規則從 IP 範圍： 127.0.0.1-127.0.0.10 新增到帳戶 "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="c9a30-109">This command adds the firewall rule named "my firewall rule" from account "ContosoAdlAcct" with the IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="c9a30-110">參數</span><span class="sxs-lookup"><span data-stu-id="c9a30-110">PARAMETERS</span></span>

### <span data-ttu-id="c9a30-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="c9a30-111">-Account</span></span>
<span data-ttu-id="c9a30-112">要新增防火牆規則的資料 Lake Analytics 帳戶</span><span class="sxs-lookup"><span data-stu-id="c9a30-112">The Data Lake Analytics account to add the firewall rule to</span></span>

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

### <span data-ttu-id="c9a30-113">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="c9a30-113">-EndIpAddress</span></span>
<span data-ttu-id="c9a30-114">防火牆規則有效 ip 範圍的結尾</span><span class="sxs-lookup"><span data-stu-id="c9a30-114">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="c9a30-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="c9a30-115">-Name</span></span>
<span data-ttu-id="c9a30-116">防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="c9a30-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="c9a30-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9a30-117">-ResourceGroupName</span></span>
<span data-ttu-id="c9a30-118">要在其下檢索帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c9a30-118">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="c9a30-119">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="c9a30-119">-StartIpAddress</span></span>
<span data-ttu-id="c9a30-120">防火牆規則的有效 ip 範圍起點</span><span class="sxs-lookup"><span data-stu-id="c9a30-120">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="c9a30-121">-確認</span><span class="sxs-lookup"><span data-stu-id="c9a30-121">-Confirm</span></span>
<span data-ttu-id="c9a30-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c9a30-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9a30-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9a30-123">-WhatIf</span></span>
<span data-ttu-id="c9a30-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c9a30-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9a30-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c9a30-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9a30-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9a30-126">-DefaultProfile</span></span>
<span data-ttu-id="c9a30-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c9a30-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9a30-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9a30-128">CommonParameters</span></span>
<span data-ttu-id="c9a30-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c9a30-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9a30-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c9a30-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9a30-131">輸入</span><span class="sxs-lookup"><span data-stu-id="c9a30-131">INPUTS</span></span>

### <span data-ttu-id="c9a30-132">System.object</span><span class="sxs-lookup"><span data-stu-id="c9a30-132">System.String</span></span>

## <span data-ttu-id="c9a30-133">輸出</span><span class="sxs-lookup"><span data-stu-id="c9a30-133">OUTPUTS</span></span>

### <span data-ttu-id="c9a30-134">DataLakeAnalyticsFirewallRule 中的 DataLakeAnalytics。</span><span class="sxs-lookup"><span data-stu-id="c9a30-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="c9a30-135">筆記</span><span class="sxs-lookup"><span data-stu-id="c9a30-135">NOTES</span></span>

## <span data-ttu-id="c9a30-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="c9a30-136">RELATED LINKS</span></span>


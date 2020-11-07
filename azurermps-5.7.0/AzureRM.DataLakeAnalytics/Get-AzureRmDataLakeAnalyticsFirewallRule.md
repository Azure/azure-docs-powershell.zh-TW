---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 49ddf65a5c32bafab32945b6d5114f65e3c59047
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623464"
---
# <span data-ttu-id="7359a-101">Get-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7359a-101">Get-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="7359a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7359a-102">SYNOPSIS</span></span>
<span data-ttu-id="7359a-103">從資料 Lake Analytics 帳戶檢索防火牆規則或防火牆規則清單。</span><span class="sxs-lookup"><span data-stu-id="7359a-103">Retrieves a firewall rule or list of firewall rules from a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7359a-104">句法</span><span class="sxs-lookup"><span data-stu-id="7359a-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7359a-105">說明</span><span class="sxs-lookup"><span data-stu-id="7359a-105">DESCRIPTION</span></span>
<span data-ttu-id="7359a-106">**AzureRmDataLakeAnalyticsFirewallRule** Cmdlet 會從 Azure Data Lake Analytics 帳戶檢索防火牆規則或防火牆規則清單。</span><span class="sxs-lookup"><span data-stu-id="7359a-106">The **Get-AzureRmDataLakeAnalyticsFirewallRule** cmdlet retrieves a firewall rule or list of firewall rules from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="7359a-107">示例</span><span class="sxs-lookup"><span data-stu-id="7359a-107">EXAMPLES</span></span>

### <span data-ttu-id="7359a-108">範例1：取得防火牆規則</span><span class="sxs-lookup"><span data-stu-id="7359a-108">Example 1: Get a firewall rule</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="7359a-109">這個命令會從帳戶 "ContosoAdlAcct" 中取得名為「我的防火牆規則」的防火牆規則</span><span class="sxs-lookup"><span data-stu-id="7359a-109">This command gets the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

### <span data-ttu-id="7359a-110">範例2：列出所有防火牆規則</span><span class="sxs-lookup"><span data-stu-id="7359a-110">Example 2: List all firewall rules</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

<span data-ttu-id="7359a-111">這個命令會從 [ContosoAdlAcct] 帳戶取得所有防火牆規則</span><span class="sxs-lookup"><span data-stu-id="7359a-111">This command gets all firewall rules from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="7359a-112">參數</span><span class="sxs-lookup"><span data-stu-id="7359a-112">PARAMETERS</span></span>

### <span data-ttu-id="7359a-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="7359a-113">-Account</span></span>
<span data-ttu-id="7359a-114">要取得防火牆規則的資料 Lake Analytics 帳戶</span><span class="sxs-lookup"><span data-stu-id="7359a-114">The Data Lake Analytics account to get the firewall rule from</span></span>

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

### <span data-ttu-id="7359a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7359a-115">-DefaultProfile</span></span>
<span data-ttu-id="7359a-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="7359a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7359a-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="7359a-117">-Name</span></span>
<span data-ttu-id="7359a-118">防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="7359a-118">The name of the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7359a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7359a-119">-ResourceGroupName</span></span>
<span data-ttu-id="7359a-120">要在其下檢索帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7359a-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="7359a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7359a-121">CommonParameters</span></span>
<span data-ttu-id="7359a-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7359a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7359a-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7359a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7359a-124">輸入</span><span class="sxs-lookup"><span data-stu-id="7359a-124">INPUTS</span></span>

### <span data-ttu-id="7359a-125">System.object</span><span class="sxs-lookup"><span data-stu-id="7359a-125">System.String</span></span>

## <span data-ttu-id="7359a-126">輸出</span><span class="sxs-lookup"><span data-stu-id="7359a-126">OUTPUTS</span></span>

### <span data-ttu-id="7359a-127">DataLakeAnalyticsFirewallRule 中的 DataLakeAnalytics。</span><span class="sxs-lookup"><span data-stu-id="7359a-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>
<span data-ttu-id="7359a-128">DataLakeAnalytics 集合. 泛型. IList "1 [DataLakeAnalyticsFirewallRule，DataLakeAnalytics，Version = 2.5.0.0，Culture = 中性，PublicKeyToken = null]] （區域性 = null）</span><span class="sxs-lookup"><span data-stu-id="7359a-128">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule, Microsoft.Azure.Commands.DataLakeAnalytics, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7359a-129">筆記</span><span class="sxs-lookup"><span data-stu-id="7359a-129">NOTES</span></span>

## <span data-ttu-id="7359a-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="7359a-130">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: c681ba089487868b556bd6e0ae198384a0dadd8c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434834"
---
# <span data-ttu-id="50f01-101">Get-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="50f01-101">Get-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="50f01-102">摘要</span><span class="sxs-lookup"><span data-stu-id="50f01-102">SYNOPSIS</span></span>
<span data-ttu-id="50f01-103">取得指定資料 Lake Store 中的指定防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="50f01-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="50f01-104">如果未指定任何防火牆規則，則會列出該帳戶的所有防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="50f01-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="50f01-105">句法</span><span class="sxs-lookup"><span data-stu-id="50f01-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50f01-106">說明</span><span class="sxs-lookup"><span data-stu-id="50f01-106">DESCRIPTION</span></span>
<span data-ttu-id="50f01-107">Get-AzDataLakeStoreFirewallRule Cmdlet 會在指定的資料 Lake Store 中取得指定的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="50f01-107">The Get-AzDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="50f01-108">如果未指定任何防火牆規則，則會列出該帳戶的所有防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="50f01-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="50f01-109">示例</span><span class="sxs-lookup"><span data-stu-id="50f01-109">EXAMPLES</span></span>

### <span data-ttu-id="50f01-110">範例1：檢索特定的防火牆規則</span><span class="sxs-lookup"><span data-stu-id="50f01-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="50f01-111">從帳戶 "ContosoADL" 傳回名為 "MyFirewallRule" 的防火牆規則</span><span class="sxs-lookup"><span data-stu-id="50f01-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="50f01-112">範例2：列出帳戶中的所有防火牆規則</span><span class="sxs-lookup"><span data-stu-id="50f01-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="50f01-113">傳回帳戶 "ContosoADL" 中的所有防火牆規則</span><span class="sxs-lookup"><span data-stu-id="50f01-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="50f01-114">參數</span><span class="sxs-lookup"><span data-stu-id="50f01-114">PARAMETERS</span></span>

### <span data-ttu-id="50f01-115">-帳戶</span><span class="sxs-lookup"><span data-stu-id="50f01-115">-Account</span></span>
<span data-ttu-id="50f01-116">要從中檢索防火牆規則的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="50f01-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

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

### <span data-ttu-id="50f01-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50f01-117">-DefaultProfile</span></span>
<span data-ttu-id="50f01-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="50f01-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50f01-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="50f01-119">-Name</span></span>
<span data-ttu-id="50f01-120">要檢索之防火牆規則的名稱</span><span class="sxs-lookup"><span data-stu-id="50f01-120">The name of the firewall rule to retrieve</span></span>

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

### <span data-ttu-id="50f01-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50f01-121">-ResourceGroupName</span></span>
<span data-ttu-id="50f01-122">要在其中檢索指定帳戶的指定防火牆規則之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="50f01-122">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

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

### <span data-ttu-id="50f01-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50f01-123">CommonParameters</span></span>
<span data-ttu-id="50f01-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="50f01-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50f01-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="50f01-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50f01-126">輸入</span><span class="sxs-lookup"><span data-stu-id="50f01-126">INPUTS</span></span>

### <span data-ttu-id="50f01-127">System.object</span><span class="sxs-lookup"><span data-stu-id="50f01-127">System.String</span></span>

## <span data-ttu-id="50f01-128">輸出</span><span class="sxs-lookup"><span data-stu-id="50f01-128">OUTPUTS</span></span>

### <span data-ttu-id="50f01-129">DataLakeStoreFirewallRule 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="50f01-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="50f01-130">筆記</span><span class="sxs-lookup"><span data-stu-id="50f01-130">NOTES</span></span>

## <span data-ttu-id="50f01-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="50f01-131">RELATED LINKS</span></span>

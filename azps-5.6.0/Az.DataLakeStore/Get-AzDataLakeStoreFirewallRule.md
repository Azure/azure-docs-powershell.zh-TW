---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 580b5518e1fc0894a51920e781464258bef9e9cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905589"
---
# <span data-ttu-id="96322-101">Get-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="96322-101">Get-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="96322-102">簡介</span><span class="sxs-lookup"><span data-stu-id="96322-102">SYNOPSIS</span></span>
<span data-ttu-id="96322-103">在指定的 Data Lake Store 中，獲得指定的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="96322-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="96322-104">如果沒有指定防火牆規則，請列出帳戶的所有防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="96322-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="96322-105">語法</span><span class="sxs-lookup"><span data-stu-id="96322-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96322-106">描述</span><span class="sxs-lookup"><span data-stu-id="96322-106">DESCRIPTION</span></span>
<span data-ttu-id="96322-107">此Get-AzDataLakeStoreFirewallRule Cmdlet 會獲得指定 Data Lake Store 中指定的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="96322-107">The Get-AzDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="96322-108">如果沒有指定防火牆規則，請列出帳戶的所有防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="96322-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="96322-109">例子</span><span class="sxs-lookup"><span data-stu-id="96322-109">EXAMPLES</span></span>

### <span data-ttu-id="96322-110">範例 1：取回特定的防火牆規則</span><span class="sxs-lookup"><span data-stu-id="96322-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="96322-111">從帳戶 "ContosoADL" 中，將防火牆規則命名為 "MyFirewallRule"</span><span class="sxs-lookup"><span data-stu-id="96322-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="96322-112">範例 2：列出帳戶的所有防火牆規則</span><span class="sxs-lookup"><span data-stu-id="96322-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="96322-113">會返回帳戶 "ContosoADL" 中所有的防火牆規則</span><span class="sxs-lookup"><span data-stu-id="96322-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="96322-114">參數</span><span class="sxs-lookup"><span data-stu-id="96322-114">PARAMETERS</span></span>

### <span data-ttu-id="96322-115">-帳戶</span><span class="sxs-lookup"><span data-stu-id="96322-115">-Account</span></span>
<span data-ttu-id="96322-116">資料湖市集帳戶，以從中取回防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="96322-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

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

### <span data-ttu-id="96322-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96322-117">-DefaultProfile</span></span>
<span data-ttu-id="96322-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="96322-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96322-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="96322-119">-Name</span></span>
<span data-ttu-id="96322-120">要取回的防火牆規則名稱</span><span class="sxs-lookup"><span data-stu-id="96322-120">The name of the firewall rule to retrieve</span></span>

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

### <span data-ttu-id="96322-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96322-121">-ResourceGroupName</span></span>
<span data-ttu-id="96322-122">想要在資源群組中取回指定帳戶指定防火牆規則的資源組名。</span><span class="sxs-lookup"><span data-stu-id="96322-122">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

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

### <span data-ttu-id="96322-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96322-123">CommonParameters</span></span>
<span data-ttu-id="96322-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="96322-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96322-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="96322-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96322-126">輸入</span><span class="sxs-lookup"><span data-stu-id="96322-126">INPUTS</span></span>

### <span data-ttu-id="96322-127">System.String</span><span class="sxs-lookup"><span data-stu-id="96322-127">System.String</span></span>

## <span data-ttu-id="96322-128">輸出</span><span class="sxs-lookup"><span data-stu-id="96322-128">OUTPUTS</span></span>

### <span data-ttu-id="96322-129">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="96322-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="96322-130">筆記</span><span class="sxs-lookup"><span data-stu-id="96322-130">NOTES</span></span>

## <span data-ttu-id="96322-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="96322-131">RELATED LINKS</span></span>

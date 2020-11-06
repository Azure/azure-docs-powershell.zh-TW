---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: e8db3842997a5bd99b970921b31d66bbbc07007a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447823"
---
# <span data-ttu-id="99de6-101">Get-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="99de6-101">Get-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="99de6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="99de6-102">SYNOPSIS</span></span>
<span data-ttu-id="99de6-103">取得指定資料 Lake Store 中的指定防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="99de6-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="99de6-104">如果未指定任何防火牆規則，則會列出該帳戶的所有防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="99de6-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99de6-105">句法</span><span class="sxs-lookup"><span data-stu-id="99de6-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99de6-106">說明</span><span class="sxs-lookup"><span data-stu-id="99de6-106">DESCRIPTION</span></span>
<span data-ttu-id="99de6-107">Get-AzureRmDataLakeStoreFirewallRule Cmdlet 會在指定的資料 Lake Store 中取得指定的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="99de6-107">The Get-AzureRmDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="99de6-108">如果未指定任何防火牆規則，則會列出該帳戶的所有防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="99de6-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="99de6-109">示例</span><span class="sxs-lookup"><span data-stu-id="99de6-109">EXAMPLES</span></span>

### <span data-ttu-id="99de6-110">範例1：檢索特定的防火牆規則</span><span class="sxs-lookup"><span data-stu-id="99de6-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="99de6-111">從帳戶 "ContosoADL" 傳回名為 "MyFirewallRule" 的防火牆規則</span><span class="sxs-lookup"><span data-stu-id="99de6-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="99de6-112">範例2：列出帳戶中的所有防火牆規則</span><span class="sxs-lookup"><span data-stu-id="99de6-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="99de6-113">傳回帳戶 "ContosoADL" 中的所有防火牆規則</span><span class="sxs-lookup"><span data-stu-id="99de6-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="99de6-114">參數</span><span class="sxs-lookup"><span data-stu-id="99de6-114">PARAMETERS</span></span>

### <span data-ttu-id="99de6-115">-帳戶</span><span class="sxs-lookup"><span data-stu-id="99de6-115">-Account</span></span>
<span data-ttu-id="99de6-116">要從中檢索防火牆規則的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="99de6-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

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

### <span data-ttu-id="99de6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99de6-117">-DefaultProfile</span></span>
<span data-ttu-id="99de6-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="99de6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99de6-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="99de6-119">-Name</span></span>
<span data-ttu-id="99de6-120">要檢索之防火牆規則的名稱</span><span class="sxs-lookup"><span data-stu-id="99de6-120">The name of the firewall rule to retrieve</span></span>

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

### <span data-ttu-id="99de6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99de6-121">-ResourceGroupName</span></span>
<span data-ttu-id="99de6-122">要在其中檢索指定帳戶的指定防火牆規則之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="99de6-122">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

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

### <span data-ttu-id="99de6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99de6-123">CommonParameters</span></span>
<span data-ttu-id="99de6-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="99de6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99de6-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="99de6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99de6-126">輸入</span><span class="sxs-lookup"><span data-stu-id="99de6-126">INPUTS</span></span>

### <span data-ttu-id="99de6-127">所有</span><span class="sxs-lookup"><span data-stu-id="99de6-127">None</span></span>
<span data-ttu-id="99de6-128">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="99de6-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="99de6-129">輸出</span><span class="sxs-lookup"><span data-stu-id="99de6-129">OUTPUTS</span></span>

### <span data-ttu-id="99de6-130">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="99de6-130">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="99de6-131">要檢索的指定防火牆規則</span><span class="sxs-lookup"><span data-stu-id="99de6-131">The specified firewall rule to retrieve</span></span>

### <span data-ttu-id="99de6-132">IList<DataLakeStoreFirewallRule></span><span class="sxs-lookup"><span data-stu-id="99de6-132">IList<DataLakeStoreFirewallRule></span></span>
<span data-ttu-id="99de6-133">指定帳戶中的防火牆規則清單。</span><span class="sxs-lookup"><span data-stu-id="99de6-133">The list of firewall rules in the specified account.</span></span>

## <span data-ttu-id="99de6-134">筆記</span><span class="sxs-lookup"><span data-stu-id="99de6-134">NOTES</span></span>

## <span data-ttu-id="99de6-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="99de6-135">RELATED LINKS</span></span>


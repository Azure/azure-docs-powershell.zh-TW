---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: C6FD4734-720C-4C8C-9B58-EDB331DD6415
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/add-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: d990f36fc68878a1751ad41ccfde51e4bbd82d2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451235"
---
# <span data-ttu-id="bff8f-101">Add-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bff8f-101">Add-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="bff8f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bff8f-102">SYNOPSIS</span></span>
<span data-ttu-id="bff8f-103">在指定的資料 Lake Store 帳戶中新增防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="bff8f-103">Adds a firewall rule to the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bff8f-104">句法</span><span class="sxs-lookup"><span data-stu-id="bff8f-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bff8f-105">說明</span><span class="sxs-lookup"><span data-stu-id="bff8f-105">DESCRIPTION</span></span>
<span data-ttu-id="bff8f-106">**AzureRmDataLakeStoreFirewallRule** Cmdlet 會在指定的資料 Lake store 帳戶中新增防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="bff8f-106">The **Add-AzureRmDataLakeStoreFirewallRule** cmdlet adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="bff8f-107">示例</span><span class="sxs-lookup"><span data-stu-id="bff8f-107">EXAMPLES</span></span>

### <span data-ttu-id="bff8f-108">範例1：將新的防火牆規則新增至 Data Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="bff8f-108">Example 1: Add a new firewall rule to a Data Lake Store account</span></span>
```
PS C:\> Add-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="bff8f-109">這會在帳戶 "ContosoADL" 中建立名為 "MyRule" 的新防火牆規則，其 IP 範圍為 127.0.0.1-127.0.0。2</span><span class="sxs-lookup"><span data-stu-id="bff8f-109">This creates a new firewall rule called "MyRule" in account "ContosoADL" with an IP range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="bff8f-110">參數</span><span class="sxs-lookup"><span data-stu-id="bff8f-110">PARAMETERS</span></span>

### <span data-ttu-id="bff8f-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="bff8f-111">-Account</span></span>
<span data-ttu-id="bff8f-112">要新增防火牆規則的 Data Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="bff8f-112">The Data Lake Store account to add the firewall rule to</span></span>

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

### <span data-ttu-id="bff8f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bff8f-113">-DefaultProfile</span></span>
<span data-ttu-id="bff8f-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="bff8f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bff8f-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="bff8f-115">-EndIpAddress</span></span>
<span data-ttu-id="bff8f-116">防火牆規則有效 ip 範圍的結尾</span><span class="sxs-lookup"><span data-stu-id="bff8f-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="bff8f-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="bff8f-117">-Name</span></span>
<span data-ttu-id="bff8f-118">要新增之防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="bff8f-118">The name of the firewall rule to add.</span></span>

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

### <span data-ttu-id="bff8f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bff8f-119">-ResourceGroupName</span></span>
<span data-ttu-id="bff8f-120">要在其中新增防火牆規則之帳戶所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bff8f-120">Name of resource group under which the account to add the firewall rule is.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bff8f-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="bff8f-121">-StartIpAddress</span></span>
<span data-ttu-id="bff8f-122">防火牆規則的有效 ip 範圍起點</span><span class="sxs-lookup"><span data-stu-id="bff8f-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="bff8f-123">-確認</span><span class="sxs-lookup"><span data-stu-id="bff8f-123">-Confirm</span></span>
<span data-ttu-id="bff8f-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bff8f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bff8f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bff8f-125">-WhatIf</span></span>
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

### <span data-ttu-id="bff8f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bff8f-126">CommonParameters</span></span>
<span data-ttu-id="bff8f-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bff8f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bff8f-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bff8f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bff8f-129">輸入</span><span class="sxs-lookup"><span data-stu-id="bff8f-129">INPUTS</span></span>

### <span data-ttu-id="bff8f-130">System.object</span><span class="sxs-lookup"><span data-stu-id="bff8f-130">System.String</span></span>

## <span data-ttu-id="bff8f-131">輸出</span><span class="sxs-lookup"><span data-stu-id="bff8f-131">OUTPUTS</span></span>

### <span data-ttu-id="bff8f-132">DataLakeStoreFirewallRule 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="bff8f-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="bff8f-133">筆記</span><span class="sxs-lookup"><span data-stu-id="bff8f-133">NOTES</span></span>

## <span data-ttu-id="bff8f-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="bff8f-134">RELATED LINKS</span></span>

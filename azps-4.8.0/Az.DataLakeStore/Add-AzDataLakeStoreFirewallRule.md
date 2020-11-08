---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: C6FD4734-720C-4C8C-9B58-EDB331DD6415
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: a13125695ab5f4c57ab2e7013d64fff376643076
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127081"
---
# <span data-ttu-id="c51e8-101">Add-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c51e8-101">Add-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="c51e8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c51e8-102">SYNOPSIS</span></span>
<span data-ttu-id="c51e8-103">在指定的資料 Lake Store 帳戶中新增防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="c51e8-103">Adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="c51e8-104">句法</span><span class="sxs-lookup"><span data-stu-id="c51e8-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c51e8-105">說明</span><span class="sxs-lookup"><span data-stu-id="c51e8-105">DESCRIPTION</span></span>
<span data-ttu-id="c51e8-106">**AzDataLakeStoreFirewallRule** Cmdlet 會在指定的資料 Lake store 帳戶中新增防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="c51e8-106">The **Add-AzDataLakeStoreFirewallRule** cmdlet adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="c51e8-107">示例</span><span class="sxs-lookup"><span data-stu-id="c51e8-107">EXAMPLES</span></span>

### <span data-ttu-id="c51e8-108">範例1：將新的防火牆規則新增至 Data Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="c51e8-108">Example 1: Add a new firewall rule to a Data Lake Store account</span></span>
```
PS C:\> Add-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="c51e8-109">這會在帳戶 "ContosoADL" 中建立名為 "MyRule" 的新防火牆規則，其 IP 範圍為 127.0.0.1-127.0.0。2</span><span class="sxs-lookup"><span data-stu-id="c51e8-109">This creates a new firewall rule called "MyRule" in account "ContosoADL" with an IP range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="c51e8-110">參數</span><span class="sxs-lookup"><span data-stu-id="c51e8-110">PARAMETERS</span></span>

### <span data-ttu-id="c51e8-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="c51e8-111">-Account</span></span>
<span data-ttu-id="c51e8-112">要新增防火牆規則的 Data Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="c51e8-112">The Data Lake Store account to add the firewall rule to</span></span>

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

### <span data-ttu-id="c51e8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c51e8-113">-DefaultProfile</span></span>
<span data-ttu-id="c51e8-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c51e8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c51e8-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="c51e8-115">-EndIpAddress</span></span>
<span data-ttu-id="c51e8-116">防火牆規則有效 ip 範圍的結尾</span><span class="sxs-lookup"><span data-stu-id="c51e8-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="c51e8-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="c51e8-117">-Name</span></span>
<span data-ttu-id="c51e8-118">要新增之防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="c51e8-118">The name of the firewall rule to add.</span></span>

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

### <span data-ttu-id="c51e8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c51e8-119">-ResourceGroupName</span></span>
<span data-ttu-id="c51e8-120">要在其中新增防火牆規則之帳戶所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c51e8-120">Name of resource group under which the account to add the firewall rule is.</span></span>

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

### <span data-ttu-id="c51e8-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="c51e8-121">-StartIpAddress</span></span>
<span data-ttu-id="c51e8-122">防火牆規則的有效 ip 範圍起點</span><span class="sxs-lookup"><span data-stu-id="c51e8-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="c51e8-123">-確認</span><span class="sxs-lookup"><span data-stu-id="c51e8-123">-Confirm</span></span>
<span data-ttu-id="c51e8-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c51e8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c51e8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c51e8-125">-WhatIf</span></span>
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

### <span data-ttu-id="c51e8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c51e8-126">CommonParameters</span></span>
<span data-ttu-id="c51e8-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c51e8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c51e8-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c51e8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c51e8-129">輸入</span><span class="sxs-lookup"><span data-stu-id="c51e8-129">INPUTS</span></span>

### <span data-ttu-id="c51e8-130">System.object</span><span class="sxs-lookup"><span data-stu-id="c51e8-130">System.String</span></span>

## <span data-ttu-id="c51e8-131">輸出</span><span class="sxs-lookup"><span data-stu-id="c51e8-131">OUTPUTS</span></span>

### <span data-ttu-id="c51e8-132">DataLakeStoreFirewallRule 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="c51e8-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="c51e8-133">筆記</span><span class="sxs-lookup"><span data-stu-id="c51e8-133">NOTES</span></span>

## <span data-ttu-id="c51e8-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="c51e8-134">RELATED LINKS</span></span>

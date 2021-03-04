---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: C6FD4734-720C-4C8C-9B58-EDB331DD6415
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/add-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 60a3363716bb4e93efa02cc63d3e83548c4944f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915517"
---
# <span data-ttu-id="0fedf-101">Add-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0fedf-101">Add-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="0fedf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0fedf-102">SYNOPSIS</span></span>
<span data-ttu-id="0fedf-103">新增防火牆規則至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="0fedf-103">Adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="0fedf-104">語法</span><span class="sxs-lookup"><span data-stu-id="0fedf-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fedf-105">描述</span><span class="sxs-lookup"><span data-stu-id="0fedf-105">DESCRIPTION</span></span>
<span data-ttu-id="0fedf-106">**Add-AzDataLakeStoreFirewallRule** Cmdlet 會新增防火牆規則至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="0fedf-106">The **Add-AzDataLakeStoreFirewallRule** cmdlet adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="0fedf-107">例子</span><span class="sxs-lookup"><span data-stu-id="0fedf-107">EXAMPLES</span></span>

### <span data-ttu-id="0fedf-108">範例 1：新增防火牆規則至 Data Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="0fedf-108">Example 1: Add a new firewall rule to a Data Lake Store account</span></span>
```
PS C:\> Add-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="0fedf-109">這會在帳戶 "ContosoADL" 中建立名為「MyRule」的新防火牆規則，其 IP 範圍為 127.0.0.1 - 127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="0fedf-109">This creates a new firewall rule called "MyRule" in account "ContosoADL" with an IP range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="0fedf-110">參數</span><span class="sxs-lookup"><span data-stu-id="0fedf-110">PARAMETERS</span></span>

### <span data-ttu-id="0fedf-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="0fedf-111">-Account</span></span>
<span data-ttu-id="0fedf-112">資料湖市集帳戶以新增防火牆規則至</span><span class="sxs-lookup"><span data-stu-id="0fedf-112">The Data Lake Store account to add the firewall rule to</span></span>

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

### <span data-ttu-id="0fedf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fedf-113">-DefaultProfile</span></span>
<span data-ttu-id="0fedf-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="0fedf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0fedf-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="0fedf-115">-EndIpAddress</span></span>
<span data-ttu-id="0fedf-116">防火牆規則的有效 ip 範圍結尾</span><span class="sxs-lookup"><span data-stu-id="0fedf-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="0fedf-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="0fedf-117">-Name</span></span>
<span data-ttu-id="0fedf-118">要新增的防火牆規則名稱。</span><span class="sxs-lookup"><span data-stu-id="0fedf-118">The name of the firewall rule to add.</span></span>

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

### <span data-ttu-id="0fedf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fedf-119">-ResourceGroupName</span></span>
<span data-ttu-id="0fedf-120">要新增防火牆規則的帳戶所根據的資源組名。</span><span class="sxs-lookup"><span data-stu-id="0fedf-120">Name of resource group under which the account to add the firewall rule is.</span></span>

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

### <span data-ttu-id="0fedf-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="0fedf-121">-StartIpAddress</span></span>
<span data-ttu-id="0fedf-122">防火牆規則的有效 ip 範圍的開始</span><span class="sxs-lookup"><span data-stu-id="0fedf-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="0fedf-123">-確認</span><span class="sxs-lookup"><span data-stu-id="0fedf-123">-Confirm</span></span>
<span data-ttu-id="0fedf-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0fedf-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fedf-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fedf-125">-WhatIf</span></span>
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

### <span data-ttu-id="0fedf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fedf-126">CommonParameters</span></span>
<span data-ttu-id="0fedf-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0fedf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fedf-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0fedf-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fedf-129">輸入</span><span class="sxs-lookup"><span data-stu-id="0fedf-129">INPUTS</span></span>

### <span data-ttu-id="0fedf-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0fedf-130">System.String</span></span>

## <span data-ttu-id="0fedf-131">輸出</span><span class="sxs-lookup"><span data-stu-id="0fedf-131">OUTPUTS</span></span>

### <span data-ttu-id="0fedf-132">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0fedf-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="0fedf-133">筆記</span><span class="sxs-lookup"><span data-stu-id="0fedf-133">NOTES</span></span>

## <span data-ttu-id="0fedf-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="0fedf-134">RELATED LINKS</span></span>

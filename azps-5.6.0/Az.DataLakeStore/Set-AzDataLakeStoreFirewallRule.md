---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: f344b7cfa893e7fffdb726df30918a27ce3366f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913237"
---
# <span data-ttu-id="ddce0-101">Set-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ddce0-101">Set-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="ddce0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ddce0-102">SYNOPSIS</span></span>
<span data-ttu-id="ddce0-103">修改指定 Data Lake Store 中指定的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="ddce0-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="ddce0-104">語法</span><span class="sxs-lookup"><span data-stu-id="ddce0-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddce0-105">描述</span><span class="sxs-lookup"><span data-stu-id="ddce0-105">DESCRIPTION</span></span>
<span data-ttu-id="ddce0-106">**Set-AzDataLakeStoreFirewallRule** Cmdlet 會修改指定 Data Lake Store 中指定的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="ddce0-106">The **Set-AzDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="ddce0-107">例子</span><span class="sxs-lookup"><span data-stu-id="ddce0-107">EXAMPLES</span></span>

### <span data-ttu-id="ddce0-108">範例 1：更新防火牆規則的開始與結束 IP 範圍</span><span class="sxs-lookup"><span data-stu-id="ddce0-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="ddce0-109">將帳戶 "ContosoADL" 中的防火牆規則「MyFirewallRule」更新為範圍 127.0.0.1 - 127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="ddce0-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="ddce0-110">參數</span><span class="sxs-lookup"><span data-stu-id="ddce0-110">PARAMETERS</span></span>

### <span data-ttu-id="ddce0-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="ddce0-111">-Account</span></span>
<span data-ttu-id="ddce0-112">Data Lake 市集帳戶以更新</span><span class="sxs-lookup"><span data-stu-id="ddce0-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="ddce0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddce0-113">-DefaultProfile</span></span>
<span data-ttu-id="ddce0-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="ddce0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ddce0-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="ddce0-115">-EndIpAddress</span></span>
<span data-ttu-id="ddce0-116">防火牆規則的有效 ip 範圍結尾</span><span class="sxs-lookup"><span data-stu-id="ddce0-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="ddce0-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="ddce0-117">-Name</span></span>
<span data-ttu-id="ddce0-118">防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="ddce0-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="ddce0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddce0-119">-ResourceGroupName</span></span>
<span data-ttu-id="ddce0-120">指定包含要更新防火牆規則之帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="ddce0-120">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

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

### <span data-ttu-id="ddce0-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="ddce0-121">-StartIpAddress</span></span>
<span data-ttu-id="ddce0-122">防火牆規則的有效 ip 範圍的開始</span><span class="sxs-lookup"><span data-stu-id="ddce0-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="ddce0-123">-確認</span><span class="sxs-lookup"><span data-stu-id="ddce0-123">-Confirm</span></span>
<span data-ttu-id="ddce0-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ddce0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddce0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddce0-125">-WhatIf</span></span>
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

### <span data-ttu-id="ddce0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddce0-126">CommonParameters</span></span>
<span data-ttu-id="ddce0-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ddce0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddce0-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ddce0-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddce0-129">輸入</span><span class="sxs-lookup"><span data-stu-id="ddce0-129">INPUTS</span></span>

### <span data-ttu-id="ddce0-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ddce0-130">System.String</span></span>

## <span data-ttu-id="ddce0-131">輸出</span><span class="sxs-lookup"><span data-stu-id="ddce0-131">OUTPUTS</span></span>

### <span data-ttu-id="ddce0-132">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ddce0-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="ddce0-133">筆記</span><span class="sxs-lookup"><span data-stu-id="ddce0-133">NOTES</span></span>

## <span data-ttu-id="ddce0-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="ddce0-134">RELATED LINKS</span></span>

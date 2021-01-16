---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 5c807c3d134768c7682b2216178eabd5a0771701
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282739"
---
# <span data-ttu-id="a9332-101">Set-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a9332-101">Set-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="a9332-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a9332-102">SYNOPSIS</span></span>
<span data-ttu-id="a9332-103">修改指定資料 Lake Store 中的指定防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="a9332-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="a9332-104">句法</span><span class="sxs-lookup"><span data-stu-id="a9332-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9332-105">說明</span><span class="sxs-lookup"><span data-stu-id="a9332-105">DESCRIPTION</span></span>
<span data-ttu-id="a9332-106">**AzDataLakeStoreFirewallRule** Cmdlet 會修改指定資料 Lake store 中的指定防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="a9332-106">The **Set-AzDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="a9332-107">示例</span><span class="sxs-lookup"><span data-stu-id="a9332-107">EXAMPLES</span></span>

### <span data-ttu-id="a9332-108">範例1：更新防火牆規則的開始和結束 IP 範圍</span><span class="sxs-lookup"><span data-stu-id="a9332-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="a9332-109">更新帳戶 "ContosoADL" 中的防火牆規則 "MyFirewallRule" 以包含127.0.0.1 範圍（127.0.0.1）127.0.0。2</span><span class="sxs-lookup"><span data-stu-id="a9332-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="a9332-110">參數</span><span class="sxs-lookup"><span data-stu-id="a9332-110">PARAMETERS</span></span>

### <span data-ttu-id="a9332-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="a9332-111">-Account</span></span>
<span data-ttu-id="a9332-112">要在其中更新防火牆規則的 Data Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="a9332-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="a9332-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9332-113">-DefaultProfile</span></span>
<span data-ttu-id="a9332-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a9332-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9332-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="a9332-115">-EndIpAddress</span></span>
<span data-ttu-id="a9332-116">防火牆規則有效 ip 範圍的結尾</span><span class="sxs-lookup"><span data-stu-id="a9332-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="a9332-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="a9332-117">-Name</span></span>
<span data-ttu-id="a9332-118">防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9332-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="a9332-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9332-119">-ResourceGroupName</span></span>
<span data-ttu-id="a9332-120">指定包含要更新防火牆規則之帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9332-120">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

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

### <span data-ttu-id="a9332-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="a9332-121">-StartIpAddress</span></span>
<span data-ttu-id="a9332-122">防火牆規則的有效 ip 範圍起點</span><span class="sxs-lookup"><span data-stu-id="a9332-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="a9332-123">-確認</span><span class="sxs-lookup"><span data-stu-id="a9332-123">-Confirm</span></span>
<span data-ttu-id="a9332-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a9332-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9332-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9332-125">-WhatIf</span></span>
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

### <span data-ttu-id="a9332-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9332-126">CommonParameters</span></span>
<span data-ttu-id="a9332-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a9332-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9332-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a9332-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9332-129">輸入</span><span class="sxs-lookup"><span data-stu-id="a9332-129">INPUTS</span></span>

### <span data-ttu-id="a9332-130">System.object</span><span class="sxs-lookup"><span data-stu-id="a9332-130">System.String</span></span>

## <span data-ttu-id="a9332-131">輸出</span><span class="sxs-lookup"><span data-stu-id="a9332-131">OUTPUTS</span></span>

### <span data-ttu-id="a9332-132">DataLakeStoreFirewallRule 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="a9332-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="a9332-133">筆記</span><span class="sxs-lookup"><span data-stu-id="a9332-133">NOTES</span></span>

## <span data-ttu-id="a9332-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9332-134">RELATED LINKS</span></span>

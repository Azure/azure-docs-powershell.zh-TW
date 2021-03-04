---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/remove-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 7a753f721e008a0c40f6a690d5c595a524ddc12b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905113"
---
# <span data-ttu-id="e7911-101">Remove-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e7911-101">Remove-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="e7911-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e7911-102">SYNOPSIS</span></span>
<span data-ttu-id="e7911-103">移除指定 Data Lake Store 中指定的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="e7911-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="e7911-104">語法</span><span class="sxs-lookup"><span data-stu-id="e7911-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7911-105">描述</span><span class="sxs-lookup"><span data-stu-id="e7911-105">DESCRIPTION</span></span>
<span data-ttu-id="e7911-106">**Remove-AzDataLakeStoreFirewallRule** Cmdlet 會移除指定 Data Lake Store 中指定的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="e7911-106">The **Remove-AzDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="e7911-107">例子</span><span class="sxs-lookup"><span data-stu-id="e7911-107">EXAMPLES</span></span>

### <span data-ttu-id="e7911-108">範例 1：從帳戶移除防火牆規則</span><span class="sxs-lookup"><span data-stu-id="e7911-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="e7911-109">從帳戶 "ContosoADL" 移除防火牆規則 "MyFirewallRule"</span><span class="sxs-lookup"><span data-stu-id="e7911-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="e7911-110">參數</span><span class="sxs-lookup"><span data-stu-id="e7911-110">PARAMETERS</span></span>

### <span data-ttu-id="e7911-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="e7911-111">-Account</span></span>
<span data-ttu-id="e7911-112">Data Lake 市集帳戶以更新</span><span class="sxs-lookup"><span data-stu-id="e7911-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="e7911-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7911-113">-DefaultProfile</span></span>
<span data-ttu-id="e7911-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="e7911-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7911-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="e7911-115">-Name</span></span>
<span data-ttu-id="e7911-116">要刪除的防火牆規則名稱。</span><span class="sxs-lookup"><span data-stu-id="e7911-116">The name of the firewall rule to delete.</span></span>

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

### <span data-ttu-id="e7911-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7911-117">-PassThru</span></span>
<span data-ttu-id="e7911-118">表示應該會返回布林值回應，指出刪除作業的結果。</span><span class="sxs-lookup"><span data-stu-id="e7911-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7911-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7911-119">-ResourceGroupName</span></span>
<span data-ttu-id="e7911-120">指定包含要移除防火牆規則之帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e7911-120">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

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

### <span data-ttu-id="e7911-121">-確認</span><span class="sxs-lookup"><span data-stu-id="e7911-121">-Confirm</span></span>
<span data-ttu-id="e7911-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e7911-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7911-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7911-123">-WhatIf</span></span>
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

### <span data-ttu-id="e7911-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7911-124">CommonParameters</span></span>
<span data-ttu-id="e7911-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e7911-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7911-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e7911-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7911-127">輸入</span><span class="sxs-lookup"><span data-stu-id="e7911-127">INPUTS</span></span>

### <span data-ttu-id="e7911-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e7911-128">System.String</span></span>

### <span data-ttu-id="e7911-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e7911-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e7911-130">輸出</span><span class="sxs-lookup"><span data-stu-id="e7911-130">OUTPUTS</span></span>

### <span data-ttu-id="e7911-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e7911-131">System.Boolean</span></span>

## <span data-ttu-id="e7911-132">筆記</span><span class="sxs-lookup"><span data-stu-id="e7911-132">NOTES</span></span>

## <span data-ttu-id="e7911-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="e7911-133">RELATED LINKS</span></span>

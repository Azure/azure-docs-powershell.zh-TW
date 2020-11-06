---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 7e762ed090b0076c5cc8d0b359cf8883ae26265d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443879"
---
# <span data-ttu-id="a251a-101">Remove-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a251a-101">Remove-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="a251a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a251a-102">SYNOPSIS</span></span>
<span data-ttu-id="a251a-103">移除指定資料 Lake Store 中的指定防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="a251a-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a251a-104">句法</span><span class="sxs-lookup"><span data-stu-id="a251a-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a251a-105">說明</span><span class="sxs-lookup"><span data-stu-id="a251a-105">DESCRIPTION</span></span>
<span data-ttu-id="a251a-106">**AzureRmDataLakeStoreFirewallRule** Cmdlet 會移除指定資料 Lake store 中的指定防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="a251a-106">The **Remove-AzureRmDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="a251a-107">示例</span><span class="sxs-lookup"><span data-stu-id="a251a-107">EXAMPLES</span></span>

### <span data-ttu-id="a251a-108">範例1：從帳戶移除防火牆規則</span><span class="sxs-lookup"><span data-stu-id="a251a-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="a251a-109">從帳戶 "ContosoADL" 移除防火牆規則 "MyFirewallRule"</span><span class="sxs-lookup"><span data-stu-id="a251a-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="a251a-110">參數</span><span class="sxs-lookup"><span data-stu-id="a251a-110">PARAMETERS</span></span>

### <span data-ttu-id="a251a-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="a251a-111">-Account</span></span>
<span data-ttu-id="a251a-112">要在其中更新防火牆規則的 Data Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="a251a-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="a251a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a251a-113">-DefaultProfile</span></span>
<span data-ttu-id="a251a-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a251a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a251a-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="a251a-115">-Name</span></span>
<span data-ttu-id="a251a-116">要刪除之防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="a251a-116">The name of the firewall rule to delete.</span></span>

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

### <span data-ttu-id="a251a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a251a-117">-PassThru</span></span>
<span data-ttu-id="a251a-118">表示應傳回指示刪除操作結果的布林回應。</span><span class="sxs-lookup"><span data-stu-id="a251a-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="a251a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a251a-119">-ResourceGroupName</span></span>
<span data-ttu-id="a251a-120">指定包含要從中移除防火牆規則之帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a251a-120">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

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

### <span data-ttu-id="a251a-121">-確認</span><span class="sxs-lookup"><span data-stu-id="a251a-121">-Confirm</span></span>
<span data-ttu-id="a251a-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a251a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a251a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a251a-123">-WhatIf</span></span>
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

### <span data-ttu-id="a251a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a251a-124">CommonParameters</span></span>
<span data-ttu-id="a251a-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a251a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a251a-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a251a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a251a-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a251a-127">INPUTS</span></span>

### <span data-ttu-id="a251a-128">System.object</span><span class="sxs-lookup"><span data-stu-id="a251a-128">System.String</span></span>

### <span data-ttu-id="a251a-129">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="a251a-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a251a-130">輸出</span><span class="sxs-lookup"><span data-stu-id="a251a-130">OUTPUTS</span></span>

### <span data-ttu-id="a251a-131">System.object</span><span class="sxs-lookup"><span data-stu-id="a251a-131">System.Boolean</span></span>

## <span data-ttu-id="a251a-132">筆記</span><span class="sxs-lookup"><span data-stu-id="a251a-132">NOTES</span></span>

## <span data-ttu-id="a251a-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="a251a-133">RELATED LINKS</span></span>

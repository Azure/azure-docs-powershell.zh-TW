---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 6bbdfa981ac1d9e80c377bf2835cff73c99a7a94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452508"
---
# <span data-ttu-id="fe357-101">Remove-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fe357-101">Remove-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="fe357-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe357-102">SYNOPSIS</span></span>
<span data-ttu-id="fe357-103">移除指定資料 Lake Store 中的指定防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="fe357-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe357-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe357-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe357-105">說明</span><span class="sxs-lookup"><span data-stu-id="fe357-105">DESCRIPTION</span></span>
<span data-ttu-id="fe357-106">**AzureRmDataLakeStoreFirewallRule** Cmdlet 會移除指定資料 Lake store 中的指定防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="fe357-106">The **Remove-AzureRmDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="fe357-107">示例</span><span class="sxs-lookup"><span data-stu-id="fe357-107">EXAMPLES</span></span>

### <span data-ttu-id="fe357-108">範例1：從帳戶移除防火牆規則</span><span class="sxs-lookup"><span data-stu-id="fe357-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="fe357-109">從帳戶 "ContosoADL" 移除防火牆規則 "MyFirewallRule"</span><span class="sxs-lookup"><span data-stu-id="fe357-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="fe357-110">參數</span><span class="sxs-lookup"><span data-stu-id="fe357-110">PARAMETERS</span></span>

### <span data-ttu-id="fe357-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="fe357-111">-Account</span></span>
<span data-ttu-id="fe357-112">要在其中更新防火牆規則的 Data Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="fe357-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="fe357-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="fe357-113">-Name</span></span>
<span data-ttu-id="fe357-114">要刪除之防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="fe357-114">The name of the firewall rule to delete.</span></span>

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

### <span data-ttu-id="fe357-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe357-115">-PassThru</span></span>
<span data-ttu-id="fe357-116">表示應傳回指示刪除操作結果的布林回應。</span><span class="sxs-lookup"><span data-stu-id="fe357-116">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="fe357-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe357-117">-ResourceGroupName</span></span>
<span data-ttu-id="fe357-118">指定包含要從中移除防火牆規則之帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fe357-118">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

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

### <span data-ttu-id="fe357-119">-確認</span><span class="sxs-lookup"><span data-stu-id="fe357-119">-Confirm</span></span>
<span data-ttu-id="fe357-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fe357-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe357-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe357-121">-WhatIf</span></span>
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

### <span data-ttu-id="fe357-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe357-122">-DefaultProfile</span></span>
<span data-ttu-id="fe357-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe357-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe357-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe357-124">CommonParameters</span></span>
<span data-ttu-id="fe357-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe357-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe357-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fe357-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe357-127">輸入</span><span class="sxs-lookup"><span data-stu-id="fe357-127">INPUTS</span></span>

## <span data-ttu-id="fe357-128">輸出</span><span class="sxs-lookup"><span data-stu-id="fe357-128">OUTPUTS</span></span>

### <span data-ttu-id="fe357-129">bool</span><span class="sxs-lookup"><span data-stu-id="fe357-129">bool</span></span>
<span data-ttu-id="fe357-130">如果已指定 PassThru，則會在成功完成時傳回 true。</span><span class="sxs-lookup"><span data-stu-id="fe357-130">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="fe357-131">筆記</span><span class="sxs-lookup"><span data-stu-id="fe357-131">NOTES</span></span>

## <span data-ttu-id="fe357-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe357-132">RELATED LINKS</span></span>

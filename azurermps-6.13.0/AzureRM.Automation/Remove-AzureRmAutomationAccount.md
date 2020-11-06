---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
ms.openlocfilehash: e3dd0d475a2a2c34dfa7912bf9ced4ef958295c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447507"
---
# <span data-ttu-id="20ac4-101">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="20ac4-101">Remove-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="20ac4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="20ac4-102">SYNOPSIS</span></span>
<span data-ttu-id="20ac4-103">移除自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="20ac4-103">Removes an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20ac4-104">句法</span><span class="sxs-lookup"><span data-stu-id="20ac4-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20ac4-105">說明</span><span class="sxs-lookup"><span data-stu-id="20ac4-105">DESCRIPTION</span></span>
<span data-ttu-id="20ac4-106">**AzureRmAutomationAccount** Cmdlet 會從資源群組中移除 Azure 自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="20ac4-106">The **Remove-AzureRmAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>
<span data-ttu-id="20ac4-107">如需自動化帳戶的詳細資訊，請參閱 New-AzureRmAutomationAccount Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="20ac4-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="20ac4-108">示例</span><span class="sxs-lookup"><span data-stu-id="20ac4-108">EXAMPLES</span></span>

### <span data-ttu-id="20ac4-109">範例1：移除自動化帳戶</span><span class="sxs-lookup"><span data-stu-id="20ac4-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="20ac4-110">這個命令會移除一個名為 ContosoAutomationAccount 的自動化帳戶，但不會提示使用者驗證。</span><span class="sxs-lookup"><span data-stu-id="20ac4-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="20ac4-111">參數</span><span class="sxs-lookup"><span data-stu-id="20ac4-111">PARAMETERS</span></span>

### <span data-ttu-id="20ac4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20ac4-112">-DefaultProfile</span></span>
<span data-ttu-id="20ac4-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="20ac4-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20ac4-114">-Force</span><span class="sxs-lookup"><span data-stu-id="20ac4-114">-Force</span></span>
<span data-ttu-id="20ac4-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="20ac4-115">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ac4-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="20ac4-116">-Name</span></span>
<span data-ttu-id="20ac4-117">指定此 Cmdlet 移除之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="20ac4-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20ac4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20ac4-118">-ResourceGroupName</span></span>
<span data-ttu-id="20ac4-119">指定此 Cmdlet 從中移除自動化帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="20ac4-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20ac4-120">-確認</span><span class="sxs-lookup"><span data-stu-id="20ac4-120">-Confirm</span></span>
<span data-ttu-id="20ac4-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="20ac4-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ac4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20ac4-122">-WhatIf</span></span>
<span data-ttu-id="20ac4-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="20ac4-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20ac4-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="20ac4-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ac4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20ac4-125">CommonParameters</span></span>
<span data-ttu-id="20ac4-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="20ac4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20ac4-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="20ac4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20ac4-128">輸入</span><span class="sxs-lookup"><span data-stu-id="20ac4-128">INPUTS</span></span>

### <span data-ttu-id="20ac4-129">System.object</span><span class="sxs-lookup"><span data-stu-id="20ac4-129">System.String</span></span>

## <span data-ttu-id="20ac4-130">輸出</span><span class="sxs-lookup"><span data-stu-id="20ac4-130">OUTPUTS</span></span>

### <span data-ttu-id="20ac4-131">AutomationAccount 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="20ac4-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="20ac4-132">筆記</span><span class="sxs-lookup"><span data-stu-id="20ac4-132">NOTES</span></span>

## <span data-ttu-id="20ac4-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="20ac4-133">RELATED LINKS</span></span>

[<span data-ttu-id="20ac4-134">AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="20ac4-134">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="20ac4-135">新-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="20ac4-135">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="20ac4-136">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="20ac4-136">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)



---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
ms.openlocfilehash: 854a5bd2fb9644d6060810edba44ac7082eb6903
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449405"
---
# <span data-ttu-id="70bf3-101">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="70bf3-101">Remove-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="70bf3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="70bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="70bf3-103">移除自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="70bf3-103">Removes an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70bf3-104">句法</span><span class="sxs-lookup"><span data-stu-id="70bf3-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70bf3-105">說明</span><span class="sxs-lookup"><span data-stu-id="70bf3-105">DESCRIPTION</span></span>
<span data-ttu-id="70bf3-106">**AzureRmAutomationAccount** Cmdlet 會從資源群組中移除 Azure 自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="70bf3-106">The **Remove-AzureRmAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>

<span data-ttu-id="70bf3-107">如需自動化帳戶的詳細資訊，請參閱 New-AzureRmAutomationAccount Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="70bf3-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="70bf3-108">示例</span><span class="sxs-lookup"><span data-stu-id="70bf3-108">EXAMPLES</span></span>

### <span data-ttu-id="70bf3-109">範例1：移除自動化帳戶</span><span class="sxs-lookup"><span data-stu-id="70bf3-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="70bf3-110">這個命令會移除一個名為 ContosoAutomationAccount 的自動化帳戶，但不會提示使用者驗證。</span><span class="sxs-lookup"><span data-stu-id="70bf3-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="70bf3-111">參數</span><span class="sxs-lookup"><span data-stu-id="70bf3-111">PARAMETERS</span></span>

### <span data-ttu-id="70bf3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70bf3-112">-DefaultProfile</span></span>
<span data-ttu-id="70bf3-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="70bf3-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70bf3-114">-Force</span><span class="sxs-lookup"><span data-stu-id="70bf3-114">-Force</span></span>
<span data-ttu-id="70bf3-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="70bf3-115">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70bf3-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="70bf3-116">-Name</span></span>
<span data-ttu-id="70bf3-117">指定此 Cmdlet 移除之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="70bf3-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70bf3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70bf3-118">-ResourceGroupName</span></span>
<span data-ttu-id="70bf3-119">指定此 Cmdlet 從中移除自動化帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="70bf3-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70bf3-120">-確認</span><span class="sxs-lookup"><span data-stu-id="70bf3-120">-Confirm</span></span>
<span data-ttu-id="70bf3-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="70bf3-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70bf3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70bf3-122">-WhatIf</span></span>
<span data-ttu-id="70bf3-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="70bf3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70bf3-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="70bf3-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70bf3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70bf3-125">CommonParameters</span></span>
<span data-ttu-id="70bf3-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="70bf3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70bf3-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="70bf3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70bf3-128">輸入</span><span class="sxs-lookup"><span data-stu-id="70bf3-128">INPUTS</span></span>

### <span data-ttu-id="70bf3-129">所有</span><span class="sxs-lookup"><span data-stu-id="70bf3-129">None</span></span>
<span data-ttu-id="70bf3-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="70bf3-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="70bf3-131">輸出</span><span class="sxs-lookup"><span data-stu-id="70bf3-131">OUTPUTS</span></span>

### <span data-ttu-id="70bf3-132">AutomationAccount 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="70bf3-132">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="70bf3-133">筆記</span><span class="sxs-lookup"><span data-stu-id="70bf3-133">NOTES</span></span>

## <span data-ttu-id="70bf3-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="70bf3-134">RELATED LINKS</span></span>

[<span data-ttu-id="70bf3-135">AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="70bf3-135">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="70bf3-136">新-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="70bf3-136">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="70bf3-137">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="70bf3-137">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)



---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
ms.openlocfilehash: 11b6772325c3e5170c697b21d25092fd96f3e2e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626171"
---
# <span data-ttu-id="5fafe-101">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5fafe-101">Remove-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="5fafe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5fafe-102">SYNOPSIS</span></span>
<span data-ttu-id="5fafe-103">移除自動化認證。</span><span class="sxs-lookup"><span data-stu-id="5fafe-103">Removes an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fafe-104">句法</span><span class="sxs-lookup"><span data-stu-id="5fafe-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5fafe-105">說明</span><span class="sxs-lookup"><span data-stu-id="5fafe-105">DESCRIPTION</span></span>
<span data-ttu-id="5fafe-106">**AzureRmAutomationCredential** Cmdlet 會從 Azure 自動化中移除認證。</span><span class="sxs-lookup"><span data-stu-id="5fafe-106">The **Remove-AzureRmAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="5fafe-107">示例</span><span class="sxs-lookup"><span data-stu-id="5fafe-107">EXAMPLES</span></span>

### <span data-ttu-id="5fafe-108">範例1：移除認證</span><span class="sxs-lookup"><span data-stu-id="5fafe-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5fafe-109">這個命令會在 Azure 自動化帳戶（名為 Contoso17）中移除一個名為 ContosoCredential 的認證。</span><span class="sxs-lookup"><span data-stu-id="5fafe-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="5fafe-110">參數</span><span class="sxs-lookup"><span data-stu-id="5fafe-110">PARAMETERS</span></span>

### <span data-ttu-id="5fafe-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5fafe-111">-AutomationAccountName</span></span>
<span data-ttu-id="5fafe-112">指定此 Cmdlet 移除認證的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="5fafe-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fafe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fafe-113">-DefaultProfile</span></span>
<span data-ttu-id="5fafe-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5fafe-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5fafe-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="5fafe-115">-Name</span></span>
<span data-ttu-id="5fafe-116">指定此 Cmdlet 移除之認證的名稱。</span><span class="sxs-lookup"><span data-stu-id="5fafe-116">Specifies the name of the credential that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fafe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fafe-117">-ResourceGroupName</span></span>
<span data-ttu-id="5fafe-118">指定此 Cmdlet 移除認證之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5fafe-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="5fafe-119">-確認</span><span class="sxs-lookup"><span data-stu-id="5fafe-119">-Confirm</span></span>
<span data-ttu-id="5fafe-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5fafe-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fafe-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fafe-121">-WhatIf</span></span>
<span data-ttu-id="5fafe-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5fafe-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fafe-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5fafe-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fafe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fafe-124">CommonParameters</span></span>
<span data-ttu-id="5fafe-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5fafe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fafe-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5fafe-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fafe-127">輸入</span><span class="sxs-lookup"><span data-stu-id="5fafe-127">INPUTS</span></span>

### <span data-ttu-id="5fafe-128">所有</span><span class="sxs-lookup"><span data-stu-id="5fafe-128">None</span></span>
<span data-ttu-id="5fafe-129">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="5fafe-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5fafe-130">輸出</span><span class="sxs-lookup"><span data-stu-id="5fafe-130">OUTPUTS</span></span>

## <span data-ttu-id="5fafe-131">筆記</span><span class="sxs-lookup"><span data-stu-id="5fafe-131">NOTES</span></span>

## <span data-ttu-id="5fafe-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="5fafe-132">RELATED LINKS</span></span>

[<span data-ttu-id="5fafe-133">AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5fafe-133">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="5fafe-134">新-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5fafe-134">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="5fafe-135">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5fafe-135">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)



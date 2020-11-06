---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
ms.openlocfilehash: 42fc322e9f593ecad6c295952d46274eb2563799
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450046"
---
# <span data-ttu-id="df73c-101">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="df73c-101">Remove-AzureRmAutomationModule</span></span>

## <span data-ttu-id="df73c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="df73c-102">SYNOPSIS</span></span>
<span data-ttu-id="df73c-103">從自動化中移除模組。</span><span class="sxs-lookup"><span data-stu-id="df73c-103">Removes a module from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df73c-104">句法</span><span class="sxs-lookup"><span data-stu-id="df73c-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df73c-105">說明</span><span class="sxs-lookup"><span data-stu-id="df73c-105">DESCRIPTION</span></span>
<span data-ttu-id="df73c-106">**AzureRmAutomationModule** Cmdlet 會從 Azure 自動化的自動化帳戶中移除模組。</span><span class="sxs-lookup"><span data-stu-id="df73c-106">The **Remove-AzureRmAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="df73c-107">示例</span><span class="sxs-lookup"><span data-stu-id="df73c-107">EXAMPLES</span></span>

### <span data-ttu-id="df73c-108">範例1：移除模組</span><span class="sxs-lookup"><span data-stu-id="df73c-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="df73c-109">這個命令會從名為 Contoso17 的自動化帳戶中移除名為 ContosoModule 的模組。</span><span class="sxs-lookup"><span data-stu-id="df73c-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="df73c-110">參數</span><span class="sxs-lookup"><span data-stu-id="df73c-110">PARAMETERS</span></span>

### <span data-ttu-id="df73c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="df73c-111">-AutomationAccountName</span></span>
<span data-ttu-id="df73c-112">指定此 Cmdlet 從中移除模組的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="df73c-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="df73c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="df73c-113">-Force</span></span>
<span data-ttu-id="df73c-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="df73c-114">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df73c-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="df73c-115">-Name</span></span>
<span data-ttu-id="df73c-116">指定此 Cmdlet 移除的模組名稱。</span><span class="sxs-lookup"><span data-stu-id="df73c-116">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="df73c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df73c-117">-ResourceGroupName</span></span>
<span data-ttu-id="df73c-118">指定此 Cmdlet 移除模組的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="df73c-118">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="df73c-119">-確認</span><span class="sxs-lookup"><span data-stu-id="df73c-119">-Confirm</span></span>
<span data-ttu-id="df73c-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="df73c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df73c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df73c-121">-WhatIf</span></span>
<span data-ttu-id="df73c-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="df73c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df73c-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="df73c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df73c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df73c-124">-DefaultProfile</span></span>
<span data-ttu-id="df73c-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="df73c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df73c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df73c-126">CommonParameters</span></span>
<span data-ttu-id="df73c-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="df73c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df73c-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="df73c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df73c-129">輸入</span><span class="sxs-lookup"><span data-stu-id="df73c-129">INPUTS</span></span>

## <span data-ttu-id="df73c-130">輸出</span><span class="sxs-lookup"><span data-stu-id="df73c-130">OUTPUTS</span></span>

## <span data-ttu-id="df73c-131">筆記</span><span class="sxs-lookup"><span data-stu-id="df73c-131">NOTES</span></span>

## <span data-ttu-id="df73c-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="df73c-132">RELATED LINKS</span></span>

[<span data-ttu-id="df73c-133">AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="df73c-133">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="df73c-134">新-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="df73c-134">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="df73c-135">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="df73c-135">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)



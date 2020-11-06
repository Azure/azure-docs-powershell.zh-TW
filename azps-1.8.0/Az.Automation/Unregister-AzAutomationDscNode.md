---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
ms.openlocfilehash: fc4696a26c10ace497c6ff64a7ac4c1ac49279c7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622926"
---
# <span data-ttu-id="5df91-101">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="5df91-101">Unregister-AzAutomationDscNode</span></span>

## <span data-ttu-id="5df91-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5df91-102">SYNOPSIS</span></span>
<span data-ttu-id="5df91-103">從管理中移除由自動化帳戶所管理的 DSC 節點。</span><span class="sxs-lookup"><span data-stu-id="5df91-103">Removes a DSC node from management by an Automation account.</span></span>

## <span data-ttu-id="5df91-104">句法</span><span class="sxs-lookup"><span data-stu-id="5df91-104">SYNTAX</span></span>

```
Unregister-AzAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5df91-105">說明</span><span class="sxs-lookup"><span data-stu-id="5df91-105">DESCRIPTION</span></span>
<span data-ttu-id="5df91-106">[ **登出 AzAutomationDscNode** ] Cmdlet 會從管理由 Azure 自動化帳戶 (DSC) 節點中移除受 Ap 所需的狀態設定。</span><span class="sxs-lookup"><span data-stu-id="5df91-106">The **Unregister-AzAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="5df91-107">示例</span><span class="sxs-lookup"><span data-stu-id="5df91-107">EXAMPLES</span></span>

### <span data-ttu-id="5df91-108">範例1：從管理中移除由自動化帳戶所管理的 Azure DSC 節點</span><span class="sxs-lookup"><span data-stu-id="5df91-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="5df91-109">這個命令會從管理中移除名為 Contoso17 的自動化帳戶的 DSC 節點，其中包含指定的 GUID。</span><span class="sxs-lookup"><span data-stu-id="5df91-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="5df91-110">參數</span><span class="sxs-lookup"><span data-stu-id="5df91-110">PARAMETERS</span></span>

### <span data-ttu-id="5df91-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5df91-111">-AutomationAccountName</span></span>
<span data-ttu-id="5df91-112">指定此 Cmdlet 從中移除 DSC 節點的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="5df91-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

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

### <span data-ttu-id="5df91-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5df91-113">-DefaultProfile</span></span>
<span data-ttu-id="5df91-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5df91-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5df91-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5df91-115">-Force</span></span>
<span data-ttu-id="5df91-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="5df91-116">ps_force</span></span>

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

### <span data-ttu-id="5df91-117">-識別碼</span><span class="sxs-lookup"><span data-stu-id="5df91-117">-Id</span></span>
<span data-ttu-id="5df91-118">指定此 Cmdlet 移除之 DSC 節點的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="5df91-118">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5df91-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5df91-119">-ResourceGroupName</span></span>
<span data-ttu-id="5df91-120">指定此 Cmdlet 在其中取消註冊 DSC 節點之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5df91-120">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

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

### <span data-ttu-id="5df91-121">-確認</span><span class="sxs-lookup"><span data-stu-id="5df91-121">-Confirm</span></span>
<span data-ttu-id="5df91-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5df91-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5df91-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5df91-123">-WhatIf</span></span>
<span data-ttu-id="5df91-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5df91-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5df91-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5df91-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5df91-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5df91-126">CommonParameters</span></span>
<span data-ttu-id="5df91-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5df91-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5df91-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5df91-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5df91-129">輸入</span><span class="sxs-lookup"><span data-stu-id="5df91-129">INPUTS</span></span>

### <span data-ttu-id="5df91-130">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="5df91-130">System.Guid</span></span>

### <span data-ttu-id="5df91-131">System.object</span><span class="sxs-lookup"><span data-stu-id="5df91-131">System.String</span></span>

## <span data-ttu-id="5df91-132">輸出</span><span class="sxs-lookup"><span data-stu-id="5df91-132">OUTPUTS</span></span>

### <span data-ttu-id="5df91-133">DscNode 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5df91-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="5df91-134">筆記</span><span class="sxs-lookup"><span data-stu-id="5df91-134">NOTES</span></span>

## <span data-ttu-id="5df91-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="5df91-135">RELATED LINKS</span></span>

[<span data-ttu-id="5df91-136">AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="5df91-136">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="5df91-137">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="5df91-137">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="5df91-138">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="5df91-138">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)



---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/unregister-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRmAutomationDscNode.md
ms.openlocfilehash: dbd70f70ec234b381f55995b9e4d31a52fe1d623
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453907"
---
# <span data-ttu-id="3acdd-101">Unregister-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3acdd-101">Unregister-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="3acdd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3acdd-102">SYNOPSIS</span></span>
<span data-ttu-id="3acdd-103">從管理中移除由自動化帳戶所管理的 DSC 節點。</span><span class="sxs-lookup"><span data-stu-id="3acdd-103">Removes a DSC node from management by an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3acdd-104">句法</span><span class="sxs-lookup"><span data-stu-id="3acdd-104">SYNTAX</span></span>

```
Unregister-AzureRmAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3acdd-105">說明</span><span class="sxs-lookup"><span data-stu-id="3acdd-105">DESCRIPTION</span></span>
<span data-ttu-id="3acdd-106">[ **登出 AzureRmAutomationDscNode** ] Cmdlet 會從管理由 Azure 自動化帳戶 (DSC) 節點中移除受 Ap 所需的狀態設定。</span><span class="sxs-lookup"><span data-stu-id="3acdd-106">The **Unregister-AzureRmAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="3acdd-107">示例</span><span class="sxs-lookup"><span data-stu-id="3acdd-107">EXAMPLES</span></span>

### <span data-ttu-id="3acdd-108">範例1：從管理中移除由自動化帳戶所管理的 Azure DSC 節點</span><span class="sxs-lookup"><span data-stu-id="3acdd-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzureRmAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="3acdd-109">這個命令會從管理中移除名為 Contoso17 的自動化帳戶的 DSC 節點，其中包含指定的 GUID。</span><span class="sxs-lookup"><span data-stu-id="3acdd-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="3acdd-110">參數</span><span class="sxs-lookup"><span data-stu-id="3acdd-110">PARAMETERS</span></span>

### <span data-ttu-id="3acdd-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3acdd-111">-AutomationAccountName</span></span>
<span data-ttu-id="3acdd-112">指定此 Cmdlet 從中移除 DSC 節點的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="3acdd-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

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

### <span data-ttu-id="3acdd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3acdd-113">-DefaultProfile</span></span>
<span data-ttu-id="3acdd-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3acdd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3acdd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3acdd-115">-Force</span></span>
<span data-ttu-id="3acdd-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="3acdd-116">ps_force</span></span>

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

### <span data-ttu-id="3acdd-117">-識別碼</span><span class="sxs-lookup"><span data-stu-id="3acdd-117">-Id</span></span>
<span data-ttu-id="3acdd-118">指定此 Cmdlet 移除之 DSC 節點的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="3acdd-118">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3acdd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3acdd-119">-ResourceGroupName</span></span>
<span data-ttu-id="3acdd-120">指定此 Cmdlet 在其中取消註冊 DSC 節點之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3acdd-120">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

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

### <span data-ttu-id="3acdd-121">-確認</span><span class="sxs-lookup"><span data-stu-id="3acdd-121">-Confirm</span></span>
<span data-ttu-id="3acdd-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3acdd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3acdd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3acdd-123">-WhatIf</span></span>
<span data-ttu-id="3acdd-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3acdd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3acdd-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3acdd-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3acdd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3acdd-126">CommonParameters</span></span>
<span data-ttu-id="3acdd-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3acdd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3acdd-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3acdd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3acdd-129">輸入</span><span class="sxs-lookup"><span data-stu-id="3acdd-129">INPUTS</span></span>

### <span data-ttu-id="3acdd-130">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="3acdd-130">System.Guid</span></span>

### <span data-ttu-id="3acdd-131">System.object</span><span class="sxs-lookup"><span data-stu-id="3acdd-131">System.String</span></span>

## <span data-ttu-id="3acdd-132">輸出</span><span class="sxs-lookup"><span data-stu-id="3acdd-132">OUTPUTS</span></span>

### <span data-ttu-id="3acdd-133">DscNode 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3acdd-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="3acdd-134">筆記</span><span class="sxs-lookup"><span data-stu-id="3acdd-134">NOTES</span></span>

## <span data-ttu-id="3acdd-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="3acdd-135">RELATED LINKS</span></span>

[<span data-ttu-id="3acdd-136">AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3acdd-136">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="3acdd-137">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3acdd-137">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="3acdd-138">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3acdd-138">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: https://docs.microsoft.com/powershell/module/az.automation/unregister-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
ms.openlocfilehash: 5c8d58024f14e2dbd1be929ddb6f156b479d2487
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911765"
---
# <span data-ttu-id="fd91b-101">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="fd91b-101">Unregister-AzAutomationDscNode</span></span>

## <span data-ttu-id="fd91b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fd91b-102">SYNOPSIS</span></span>
<span data-ttu-id="fd91b-103">使用自動化帳戶從管理移除 DSC 節點。</span><span class="sxs-lookup"><span data-stu-id="fd91b-103">Removes a DSC node from management by an Automation account.</span></span>

## <span data-ttu-id="fd91b-104">語法</span><span class="sxs-lookup"><span data-stu-id="fd91b-104">SYNTAX</span></span>

```
Unregister-AzAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd91b-105">描述</span><span class="sxs-lookup"><span data-stu-id="fd91b-105">DESCRIPTION</span></span>
<span data-ttu-id="fd91b-106">**取消註冊-AzAutomationDscNode** Cmdlet 會移除 Azure Automation 帳戶管理中的 APS 想要狀態組態 (DSC) 節點。</span><span class="sxs-lookup"><span data-stu-id="fd91b-106">The **Unregister-AzAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="fd91b-107">例子</span><span class="sxs-lookup"><span data-stu-id="fd91b-107">EXAMPLES</span></span>

### <span data-ttu-id="fd91b-108">範例 1：使用自動化帳戶從管理移除 Azure DSC 節點</span><span class="sxs-lookup"><span data-stu-id="fd91b-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="fd91b-109">此命令會從名為 Contoso17 的自動化帳戶管理移除具有指定 GUID 的 DSC 節點。</span><span class="sxs-lookup"><span data-stu-id="fd91b-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="fd91b-110">參數</span><span class="sxs-lookup"><span data-stu-id="fd91b-110">PARAMETERS</span></span>

### <span data-ttu-id="fd91b-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fd91b-111">-AutomationAccountName</span></span>
<span data-ttu-id="fd91b-112">指定此 Cmdlet 移除 DSC 節點的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="fd91b-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

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

### <span data-ttu-id="fd91b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd91b-113">-DefaultProfile</span></span>
<span data-ttu-id="fd91b-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="fd91b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd91b-115">-強制</span><span class="sxs-lookup"><span data-stu-id="fd91b-115">-Force</span></span>
<span data-ttu-id="fd91b-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="fd91b-116">ps_force</span></span>

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

### <span data-ttu-id="fd91b-117">-Id</span><span class="sxs-lookup"><span data-stu-id="fd91b-117">-Id</span></span>
<span data-ttu-id="fd91b-118">指定此 Cmdlet 移除之 DSC 節點的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="fd91b-118">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fd91b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd91b-119">-ResourceGroupName</span></span>
<span data-ttu-id="fd91b-120">指定此 Cmdlet 取消註冊 DSC 節點的資源組名。</span><span class="sxs-lookup"><span data-stu-id="fd91b-120">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

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

### <span data-ttu-id="fd91b-121">-確認</span><span class="sxs-lookup"><span data-stu-id="fd91b-121">-Confirm</span></span>
<span data-ttu-id="fd91b-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fd91b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd91b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd91b-123">-WhatIf</span></span>
<span data-ttu-id="fd91b-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fd91b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd91b-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fd91b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd91b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd91b-126">CommonParameters</span></span>
<span data-ttu-id="fd91b-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fd91b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd91b-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="fd91b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd91b-129">輸入</span><span class="sxs-lookup"><span data-stu-id="fd91b-129">INPUTS</span></span>

### <span data-ttu-id="fd91b-130">System.Guid</span><span class="sxs-lookup"><span data-stu-id="fd91b-130">System.Guid</span></span>

### <span data-ttu-id="fd91b-131">System.String</span><span class="sxs-lookup"><span data-stu-id="fd91b-131">System.String</span></span>

## <span data-ttu-id="fd91b-132">輸出</span><span class="sxs-lookup"><span data-stu-id="fd91b-132">OUTPUTS</span></span>

### <span data-ttu-id="fd91b-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span><span class="sxs-lookup"><span data-stu-id="fd91b-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="fd91b-134">筆記</span><span class="sxs-lookup"><span data-stu-id="fd91b-134">NOTES</span></span>

## <span data-ttu-id="fd91b-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="fd91b-135">RELATED LINKS</span></span>

[<span data-ttu-id="fd91b-136">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="fd91b-136">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="fd91b-137">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="fd91b-137">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="fd91b-138">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="fd91b-138">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)



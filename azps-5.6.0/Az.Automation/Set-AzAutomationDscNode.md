---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 60023C8D-EA37-41DA-97E6-AF89F7F9BADD
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationDscNode.md
ms.openlocfilehash: 5aa70f15b5f542b36420e5f8df1cc65bb5dbd09a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915637"
---
# <span data-ttu-id="cc1ea-101">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="cc1ea-101">Set-AzAutomationDscNode</span></span>

## <span data-ttu-id="cc1ea-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cc1ea-102">SYNOPSIS</span></span>
<span data-ttu-id="cc1ea-103">修改 DSC 節點對應至的節點群組原則。</span><span class="sxs-lookup"><span data-stu-id="cc1ea-103">Modifies the node configuration that a DSC node is mapped to.</span></span>

## <span data-ttu-id="cc1ea-104">語法</span><span class="sxs-lookup"><span data-stu-id="cc1ea-104">SYNTAX</span></span>

```
Set-AzAutomationDscNode -Id <Guid> -NodeConfigurationName <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cc1ea-105">描述</span><span class="sxs-lookup"><span data-stu-id="cc1ea-105">DESCRIPTION</span></span>
<span data-ttu-id="cc1ea-106">**Set-AzAutomationDscNode** Cmdlet 會修改 APS (狀態設定) 節點設定。</span><span class="sxs-lookup"><span data-stu-id="cc1ea-106">The **Set-AzAutomationDscNode** cmdlet modifies an APS Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="cc1ea-107">Azure Automation 會以受管理的物件格式將 DSC 節點組 (MOF) 設定檔。</span><span class="sxs-lookup"><span data-stu-id="cc1ea-107">Azure Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="cc1ea-108">例子</span><span class="sxs-lookup"><span data-stu-id="cc1ea-108">EXAMPLES</span></span>

### <span data-ttu-id="cc1ea-109">範例 1：修改節點組配置地圖</span><span class="sxs-lookup"><span data-stu-id="cc1ea-109">Example 1: Modify node configuration mapping</span></span>
```
PS C:\>Set-AzAutomationDscNode -NodeConfigurationName "Contoso.NodeConfiguration01" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111c8a6067j8
```

<span data-ttu-id="cc1ea-110">此命令會指派名為 Contoso.NodeConfiguration01 的節點組配置給具有指定 GUID 的節點。</span><span class="sxs-lookup"><span data-stu-id="cc1ea-110">This command assigns the node configuration named Contoso.NodeConfiguration01 to the node that has the specified GUID.</span></span>

## <span data-ttu-id="cc1ea-111">參數</span><span class="sxs-lookup"><span data-stu-id="cc1ea-111">PARAMETERS</span></span>

### <span data-ttu-id="cc1ea-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cc1ea-112">-AutomationAccountName</span></span>
<span data-ttu-id="cc1ea-113">指定包含此 Cmdlet 修改該配置的 DSC 節點的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="cc1ea-113">Specifies the name of the Automation account that contains the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="cc1ea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc1ea-114">-DefaultProfile</span></span>
<span data-ttu-id="cc1ea-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="cc1ea-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc1ea-116">-強制</span><span class="sxs-lookup"><span data-stu-id="cc1ea-116">-Force</span></span>
<span data-ttu-id="cc1ea-117">ps_force命令執行，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="cc1ea-117">ps_force the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cc1ea-118">-Id</span><span class="sxs-lookup"><span data-stu-id="cc1ea-118">-Id</span></span>
<span data-ttu-id="cc1ea-119">指定此 Cmdlet 修改該配置的 DSC 節點的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="cc1ea-119">Specifies the unique ID of the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="cc1ea-120">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="cc1ea-120">-NodeConfigurationName</span></span>
<span data-ttu-id="cc1ea-121">指定此 Cmdlet 與節點進行地圖的節點群組原則名稱。</span><span class="sxs-lookup"><span data-stu-id="cc1ea-121">Specifies the name of the node configuration to which this cmdlet maps the node.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc1ea-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc1ea-122">-ResourceGroupName</span></span>
<span data-ttu-id="cc1ea-123">指定此 Cmdlet 修改 DSC 節點組配置的資源組名。</span><span class="sxs-lookup"><span data-stu-id="cc1ea-123">Specifies the name of a resource group in which this cmdlet modifies a DSC node configuration.</span></span>

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

### <span data-ttu-id="cc1ea-124">-確認</span><span class="sxs-lookup"><span data-stu-id="cc1ea-124">-Confirm</span></span>
<span data-ttu-id="cc1ea-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cc1ea-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc1ea-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc1ea-126">-WhatIf</span></span>
<span data-ttu-id="cc1ea-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cc1ea-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc1ea-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc1ea-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc1ea-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc1ea-129">CommonParameters</span></span>
<span data-ttu-id="cc1ea-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cc1ea-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc1ea-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="cc1ea-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc1ea-132">輸入</span><span class="sxs-lookup"><span data-stu-id="cc1ea-132">INPUTS</span></span>

### <span data-ttu-id="cc1ea-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="cc1ea-133">System.Guid</span></span>

### <span data-ttu-id="cc1ea-134">System.String</span><span class="sxs-lookup"><span data-stu-id="cc1ea-134">System.String</span></span>

## <span data-ttu-id="cc1ea-135">輸出</span><span class="sxs-lookup"><span data-stu-id="cc1ea-135">OUTPUTS</span></span>

### <span data-ttu-id="cc1ea-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span><span class="sxs-lookup"><span data-stu-id="cc1ea-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="cc1ea-137">筆記</span><span class="sxs-lookup"><span data-stu-id="cc1ea-137">NOTES</span></span>

## <span data-ttu-id="cc1ea-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc1ea-138">RELATED LINKS</span></span>

[<span data-ttu-id="cc1ea-139">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="cc1ea-139">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="cc1ea-140">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="cc1ea-140">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="cc1ea-141">取消註冊-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="cc1ea-141">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)



---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 60023C8D-EA37-41DA-97E6-AF89F7F9BADD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationDscNode.md
ms.openlocfilehash: 663573e7f4e111880c5ed0014dcad18480f665ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623836"
---
# <span data-ttu-id="b29dd-101">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b29dd-101">Set-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="b29dd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b29dd-102">SYNOPSIS</span></span>
<span data-ttu-id="b29dd-103">修改與 DSC 節點對應的節點設定。</span><span class="sxs-lookup"><span data-stu-id="b29dd-103">Modifies the node configuration that a DSC node is mapped to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b29dd-104">句法</span><span class="sxs-lookup"><span data-stu-id="b29dd-104">SYNTAX</span></span>

```
Set-AzureRmAutomationDscNode -Id <Guid> -NodeConfigurationName <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b29dd-105">說明</span><span class="sxs-lookup"><span data-stu-id="b29dd-105">DESCRIPTION</span></span>
<span data-ttu-id="b29dd-106">**AzureRmAutomationDscNode** Cmdlet 會修改 (DSC) 節點設定的 Ap 所需狀態設定。</span><span class="sxs-lookup"><span data-stu-id="b29dd-106">The **Set-AzureRmAutomationDscNode** cmdlet modifies an APS Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="b29dd-107">Azure 自動化會將 DSC 節點設定儲存為受管理的物件格式， (MOF) 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b29dd-107">Azure Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="b29dd-108">示例</span><span class="sxs-lookup"><span data-stu-id="b29dd-108">EXAMPLES</span></span>

### <span data-ttu-id="b29dd-109">範例1：修改節點配置對應</span><span class="sxs-lookup"><span data-stu-id="b29dd-109">Example 1: Modify node configuration mapping</span></span>
```
PS C:\>Set-AzureRmAutomationDscNode -NodeConfigurationName "Contoso.NodeConfiguration01" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111c8a6067j8
```

<span data-ttu-id="b29dd-110">這個命令會將名為 NodeConfiguration01 的節點配置指派給具有指定 GUID 的節點。</span><span class="sxs-lookup"><span data-stu-id="b29dd-110">This command assigns the node configuration named Contoso.NodeConfiguration01 to the node that has the specified GUID.</span></span>

## <span data-ttu-id="b29dd-111">參數</span><span class="sxs-lookup"><span data-stu-id="b29dd-111">PARAMETERS</span></span>

### <span data-ttu-id="b29dd-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b29dd-112">-AutomationAccountName</span></span>
<span data-ttu-id="b29dd-113">指定包含此 Cmdlet 修改設定之 DSC 節點之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="b29dd-113">Specifies the name of the Automation account that contains the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="b29dd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b29dd-114">-DefaultProfile</span></span>
<span data-ttu-id="b29dd-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b29dd-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b29dd-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b29dd-116">-Force</span></span>
<span data-ttu-id="b29dd-117">ps_force 執行命令，不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b29dd-117">ps_force the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b29dd-118">-識別碼</span><span class="sxs-lookup"><span data-stu-id="b29dd-118">-Id</span></span>
<span data-ttu-id="b29dd-119">指定此 Cmdlet 修改配置的 DSC 節點的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="b29dd-119">Specifies the unique ID of the DSC node for which this cmdlet modifies the configuration.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b29dd-120">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="b29dd-120">-NodeConfigurationName</span></span>
<span data-ttu-id="b29dd-121">指定此 Cmdlet 對應節點的節點配置名稱。</span><span class="sxs-lookup"><span data-stu-id="b29dd-121">Specifies the name of the node configuration to which this cmdlet maps the node.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b29dd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b29dd-122">-ResourceGroupName</span></span>
<span data-ttu-id="b29dd-123">指定此 Cmdlet 修改 DSC 節點設定之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b29dd-123">Specifies the name of a resource group in which this cmdlet modifies a DSC node configuration.</span></span>

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

### <span data-ttu-id="b29dd-124">-確認</span><span class="sxs-lookup"><span data-stu-id="b29dd-124">-Confirm</span></span>
<span data-ttu-id="b29dd-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b29dd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b29dd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b29dd-126">-WhatIf</span></span>
<span data-ttu-id="b29dd-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b29dd-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b29dd-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b29dd-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b29dd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b29dd-129">CommonParameters</span></span>
<span data-ttu-id="b29dd-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b29dd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b29dd-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b29dd-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b29dd-132">輸入</span><span class="sxs-lookup"><span data-stu-id="b29dd-132">INPUTS</span></span>

### <span data-ttu-id="b29dd-133">所有</span><span class="sxs-lookup"><span data-stu-id="b29dd-133">None</span></span>
<span data-ttu-id="b29dd-134">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="b29dd-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b29dd-135">輸出</span><span class="sxs-lookup"><span data-stu-id="b29dd-135">OUTPUTS</span></span>

### <span data-ttu-id="b29dd-136">DscNode 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b29dd-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="b29dd-137">筆記</span><span class="sxs-lookup"><span data-stu-id="b29dd-137">NOTES</span></span>

## <span data-ttu-id="b29dd-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="b29dd-138">RELATED LINKS</span></span>

[<span data-ttu-id="b29dd-139">AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b29dd-139">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="b29dd-140">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b29dd-140">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="b29dd-141">取消註冊-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b29dd-141">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)



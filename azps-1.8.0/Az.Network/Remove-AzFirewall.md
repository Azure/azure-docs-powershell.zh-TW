---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
ms.openlocfilehash: b46540a614f25a3923301e28cd19d8f1b76af53c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621612"
---
# <span data-ttu-id="5b8ef-101">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="5b8ef-101">Remove-AzFirewall</span></span>

## <span data-ttu-id="5b8ef-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5b8ef-102">SYNOPSIS</span></span>
<span data-ttu-id="5b8ef-103">移除防火牆。</span><span class="sxs-lookup"><span data-stu-id="5b8ef-103">Remove a Firewall.</span></span>

## <span data-ttu-id="5b8ef-104">句法</span><span class="sxs-lookup"><span data-stu-id="5b8ef-104">SYNTAX</span></span>

```
Remove-AzFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b8ef-105">說明</span><span class="sxs-lookup"><span data-stu-id="5b8ef-105">DESCRIPTION</span></span>
<span data-ttu-id="5b8ef-106">**AzFirewall** Cmdlet 會移除 Azure 防火牆。</span><span class="sxs-lookup"><span data-stu-id="5b8ef-106">The **Remove-AzFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="5b8ef-107">示例</span><span class="sxs-lookup"><span data-stu-id="5b8ef-107">EXAMPLES</span></span>

### <span data-ttu-id="5b8ef-108">1：建立及刪除防火牆</span><span class="sxs-lookup"><span data-stu-id="5b8ef-108">1: Create and delete a Firewall</span></span>
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="5b8ef-109">這個範例會建立防火牆，然後將它刪除。</span><span class="sxs-lookup"><span data-stu-id="5b8ef-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="5b8ef-110">若要在刪除防火牆時取消提示，請使用-Force 標誌。</span><span class="sxs-lookup"><span data-stu-id="5b8ef-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

### <span data-ttu-id="5b8ef-111">2：解除配置防火牆，然後刪除防火牆</span><span class="sxs-lookup"><span data-stu-id="5b8ef-111">2: Deallocate the Firewall, then delete the Firewall</span></span>
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
Remove-AzFirewall -ResourceGroupName rgName -Name azFw
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="5b8ef-112">這個範例會檢索防火牆、解除防火牆的釋放，然後刪除防火牆。</span><span class="sxs-lookup"><span data-stu-id="5b8ef-112">This example retrieves a Firewall, deallocates the firewall, and then deletes the firewall.</span></span> <span data-ttu-id="5b8ef-113">解除配置命令會移除執行中的服務，但會保留防火牆的設定。</span><span class="sxs-lookup"><span data-stu-id="5b8ef-113">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="5b8ef-114">如果使用者想要再次啟動服務，請在防火牆上呼叫 Allocate 方法。</span><span class="sxs-lookup"><span data-stu-id="5b8ef-114">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="5b8ef-115">若要在刪除防火牆時取消提示，請使用-Force 標誌。</span><span class="sxs-lookup"><span data-stu-id="5b8ef-115">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="5b8ef-116">參數</span><span class="sxs-lookup"><span data-stu-id="5b8ef-116">PARAMETERS</span></span>

### <span data-ttu-id="5b8ef-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b8ef-117">-AsJob</span></span>
<span data-ttu-id="5b8ef-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5b8ef-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5b8ef-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b8ef-119">-DefaultProfile</span></span>
<span data-ttu-id="5b8ef-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5b8ef-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b8ef-121">-Force</span><span class="sxs-lookup"><span data-stu-id="5b8ef-121">-Force</span></span>
<span data-ttu-id="5b8ef-122">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="5b8ef-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5b8ef-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="5b8ef-123">-Name</span></span>
<span data-ttu-id="5b8ef-124">指定此 Cmdlet 移除的防火牆名稱。</span><span class="sxs-lookup"><span data-stu-id="5b8ef-124">Specifies the name of the firewall that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b8ef-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b8ef-125">-PassThru</span></span>
<span data-ttu-id="5b8ef-126">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="5b8ef-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5b8ef-127">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="5b8ef-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5b8ef-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b8ef-128">-ResourceGroupName</span></span>
<span data-ttu-id="5b8ef-129">指定包含此 Cmdlet 移除之防火牆之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b8ef-129">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5b8ef-130">-確認</span><span class="sxs-lookup"><span data-stu-id="5b8ef-130">-Confirm</span></span>
<span data-ttu-id="5b8ef-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5b8ef-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b8ef-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b8ef-132">-WhatIf</span></span>
<span data-ttu-id="5b8ef-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5b8ef-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b8ef-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5b8ef-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b8ef-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b8ef-135">CommonParameters</span></span>
<span data-ttu-id="5b8ef-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5b8ef-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b8ef-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5b8ef-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b8ef-138">輸入</span><span class="sxs-lookup"><span data-stu-id="5b8ef-138">INPUTS</span></span>

### <span data-ttu-id="5b8ef-139">System.object</span><span class="sxs-lookup"><span data-stu-id="5b8ef-139">System.String</span></span>

## <span data-ttu-id="5b8ef-140">輸出</span><span class="sxs-lookup"><span data-stu-id="5b8ef-140">OUTPUTS</span></span>

### <span data-ttu-id="5b8ef-141">System.object</span><span class="sxs-lookup"><span data-stu-id="5b8ef-141">System.Boolean</span></span>

## <span data-ttu-id="5b8ef-142">筆記</span><span class="sxs-lookup"><span data-stu-id="5b8ef-142">NOTES</span></span>

## <span data-ttu-id="5b8ef-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b8ef-143">RELATED LINKS</span></span>

[<span data-ttu-id="5b8ef-144">AzFirewall</span><span class="sxs-lookup"><span data-stu-id="5b8ef-144">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="5b8ef-145">新-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="5b8ef-145">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="5b8ef-146">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="5b8ef-146">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

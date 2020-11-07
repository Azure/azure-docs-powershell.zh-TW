---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
ms.openlocfilehash: b5b4c06c3f409bbe6642386420301c899eb43000
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790669"
---
# <span data-ttu-id="a4f7d-101">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a4f7d-101">Remove-AzFirewall</span></span>

## <span data-ttu-id="a4f7d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a4f7d-102">SYNOPSIS</span></span>
<span data-ttu-id="a4f7d-103">移除防火牆。</span><span class="sxs-lookup"><span data-stu-id="a4f7d-103">Remove a Firewall.</span></span>

## <span data-ttu-id="a4f7d-104">句法</span><span class="sxs-lookup"><span data-stu-id="a4f7d-104">SYNTAX</span></span>

```
Remove-AzFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4f7d-105">說明</span><span class="sxs-lookup"><span data-stu-id="a4f7d-105">DESCRIPTION</span></span>
<span data-ttu-id="a4f7d-106">**AzFirewall** Cmdlet 會移除 Azure 防火牆。</span><span class="sxs-lookup"><span data-stu-id="a4f7d-106">The **Remove-AzFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="a4f7d-107">示例</span><span class="sxs-lookup"><span data-stu-id="a4f7d-107">EXAMPLES</span></span>

### <span data-ttu-id="a4f7d-108">1：建立及刪除防火牆</span><span class="sxs-lookup"><span data-stu-id="a4f7d-108">1: Create and delete a Firewall</span></span>
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="a4f7d-109">這個範例會建立防火牆，然後將它刪除。</span><span class="sxs-lookup"><span data-stu-id="a4f7d-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="a4f7d-110">若要在刪除防火牆時取消提示，請使用-Force 標誌。</span><span class="sxs-lookup"><span data-stu-id="a4f7d-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="a4f7d-111">參數</span><span class="sxs-lookup"><span data-stu-id="a4f7d-111">PARAMETERS</span></span>

### <span data-ttu-id="a4f7d-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4f7d-112">-AsJob</span></span>
<span data-ttu-id="a4f7d-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a4f7d-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a4f7d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4f7d-114">-DefaultProfile</span></span>
<span data-ttu-id="a4f7d-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a4f7d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4f7d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a4f7d-116">-Force</span></span>
<span data-ttu-id="a4f7d-117">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="a4f7d-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a4f7d-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="a4f7d-118">-Name</span></span>
<span data-ttu-id="a4f7d-119">指定此 Cmdlet 移除的防火牆名稱。</span><span class="sxs-lookup"><span data-stu-id="a4f7d-119">Specifies the name of the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a4f7d-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4f7d-120">-PassThru</span></span>
<span data-ttu-id="a4f7d-121">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="a4f7d-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a4f7d-122">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="a4f7d-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a4f7d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4f7d-123">-ResourceGroupName</span></span>
<span data-ttu-id="a4f7d-124">指定包含此 Cmdlet 移除之防火牆之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a4f7d-124">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a4f7d-125">-確認</span><span class="sxs-lookup"><span data-stu-id="a4f7d-125">-Confirm</span></span>
<span data-ttu-id="a4f7d-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a4f7d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4f7d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4f7d-127">-WhatIf</span></span>
<span data-ttu-id="a4f7d-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a4f7d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4f7d-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a4f7d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4f7d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4f7d-130">CommonParameters</span></span>
<span data-ttu-id="a4f7d-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a4f7d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4f7d-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a4f7d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4f7d-133">輸入</span><span class="sxs-lookup"><span data-stu-id="a4f7d-133">INPUTS</span></span>

### <span data-ttu-id="a4f7d-134">System.object</span><span class="sxs-lookup"><span data-stu-id="a4f7d-134">System.String</span></span>

## <span data-ttu-id="a4f7d-135">輸出</span><span class="sxs-lookup"><span data-stu-id="a4f7d-135">OUTPUTS</span></span>

### <span data-ttu-id="a4f7d-136">System.object</span><span class="sxs-lookup"><span data-stu-id="a4f7d-136">System.Boolean</span></span>

## <span data-ttu-id="a4f7d-137">筆記</span><span class="sxs-lookup"><span data-stu-id="a4f7d-137">NOTES</span></span>

## <span data-ttu-id="a4f7d-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4f7d-138">RELATED LINKS</span></span>

[<span data-ttu-id="a4f7d-139">AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a4f7d-139">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="a4f7d-140">新-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a4f7d-140">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="a4f7d-141">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a4f7d-141">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

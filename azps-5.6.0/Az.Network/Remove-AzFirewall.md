---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
ms.openlocfilehash: 4be419ab76180174fd6132335822c361008ec872
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912702"
---
# <span data-ttu-id="51fbc-101">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="51fbc-101">Remove-AzFirewall</span></span>

## <span data-ttu-id="51fbc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="51fbc-102">SYNOPSIS</span></span>
<span data-ttu-id="51fbc-103">移除防火牆。</span><span class="sxs-lookup"><span data-stu-id="51fbc-103">Remove a Firewall.</span></span>

## <span data-ttu-id="51fbc-104">語法</span><span class="sxs-lookup"><span data-stu-id="51fbc-104">SYNTAX</span></span>

```
Remove-AzFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51fbc-105">描述</span><span class="sxs-lookup"><span data-stu-id="51fbc-105">DESCRIPTION</span></span>
<span data-ttu-id="51fbc-106">**Remove-AzFirewall** Cmdlet 會移除 Azure 防火牆。</span><span class="sxs-lookup"><span data-stu-id="51fbc-106">The **Remove-AzFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="51fbc-107">例子</span><span class="sxs-lookup"><span data-stu-id="51fbc-107">EXAMPLES</span></span>

### <span data-ttu-id="51fbc-108">範例 1：建立及刪除防火牆</span><span class="sxs-lookup"><span data-stu-id="51fbc-108">Example 1: Create and delete a Firewall</span></span>
```powershell
New-AzFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="51fbc-109">此範例會建立防火牆，然後將其刪除。</span><span class="sxs-lookup"><span data-stu-id="51fbc-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="51fbc-110">若要隱藏刪除防火牆時提示，請使用 -Force 旗標。</span><span class="sxs-lookup"><span data-stu-id="51fbc-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="51fbc-111">參數</span><span class="sxs-lookup"><span data-stu-id="51fbc-111">PARAMETERS</span></span>

### <span data-ttu-id="51fbc-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51fbc-112">-AsJob</span></span>
<span data-ttu-id="51fbc-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="51fbc-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51fbc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51fbc-114">-DefaultProfile</span></span>
<span data-ttu-id="51fbc-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="51fbc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51fbc-116">-強制</span><span class="sxs-lookup"><span data-stu-id="51fbc-116">-Force</span></span>
<span data-ttu-id="51fbc-117">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="51fbc-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="51fbc-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="51fbc-118">-Name</span></span>
<span data-ttu-id="51fbc-119">指定此 Cmdlet 移除的防火牆名稱。</span><span class="sxs-lookup"><span data-stu-id="51fbc-119">Specifies the name of the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="51fbc-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51fbc-120">-PassThru</span></span>
<span data-ttu-id="51fbc-121">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="51fbc-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="51fbc-122">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="51fbc-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="51fbc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51fbc-123">-ResourceGroupName</span></span>
<span data-ttu-id="51fbc-124">指定包含此 Cmdlet 移除之防火牆的資源組名。</span><span class="sxs-lookup"><span data-stu-id="51fbc-124">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="51fbc-125">-確認</span><span class="sxs-lookup"><span data-stu-id="51fbc-125">-Confirm</span></span>
<span data-ttu-id="51fbc-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="51fbc-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51fbc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51fbc-127">-WhatIf</span></span>
<span data-ttu-id="51fbc-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="51fbc-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51fbc-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="51fbc-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51fbc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51fbc-130">CommonParameters</span></span>
<span data-ttu-id="51fbc-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="51fbc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51fbc-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="51fbc-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51fbc-133">輸入</span><span class="sxs-lookup"><span data-stu-id="51fbc-133">INPUTS</span></span>

### <span data-ttu-id="51fbc-134">System.String</span><span class="sxs-lookup"><span data-stu-id="51fbc-134">System.String</span></span>

## <span data-ttu-id="51fbc-135">輸出</span><span class="sxs-lookup"><span data-stu-id="51fbc-135">OUTPUTS</span></span>

### <span data-ttu-id="51fbc-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="51fbc-136">System.Boolean</span></span>

## <span data-ttu-id="51fbc-137">筆記</span><span class="sxs-lookup"><span data-stu-id="51fbc-137">NOTES</span></span>

## <span data-ttu-id="51fbc-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="51fbc-138">RELATED LINKS</span></span>

[<span data-ttu-id="51fbc-139">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="51fbc-139">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="51fbc-140">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="51fbc-140">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="51fbc-141">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="51fbc-141">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

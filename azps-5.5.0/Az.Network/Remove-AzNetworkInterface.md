---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
ms.openlocfilehash: f4de49bb2e35bf3d392fba06d663800a5bdc44a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131154"
---
# <span data-ttu-id="e2269-101">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e2269-101">Remove-AzNetworkInterface</span></span>

## <span data-ttu-id="e2269-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e2269-102">SYNOPSIS</span></span>
<span data-ttu-id="e2269-103">移除網路介面。</span><span class="sxs-lookup"><span data-stu-id="e2269-103">Removes a network interface.</span></span>

## <span data-ttu-id="e2269-104">句法</span><span class="sxs-lookup"><span data-stu-id="e2269-104">SYNTAX</span></span>

```
Remove-AzNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2269-105">說明</span><span class="sxs-lookup"><span data-stu-id="e2269-105">DESCRIPTION</span></span>
<span data-ttu-id="e2269-106">**AzNetworkInterface** Cmdlet 會移除 Azure 網路介面。</span><span class="sxs-lookup"><span data-stu-id="e2269-106">The **Remove-AzNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="e2269-107">示例</span><span class="sxs-lookup"><span data-stu-id="e2269-107">EXAMPLES</span></span>

### <span data-ttu-id="e2269-108">範例1：移除網路介面</span><span class="sxs-lookup"><span data-stu-id="e2269-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="e2269-109">這個命令會移除 [資源群組 ResourceGroup1] 中的 [網路介面 NetworkInterface1]。</span><span class="sxs-lookup"><span data-stu-id="e2269-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="e2269-110">由於不使用 *Force* 參數，系統會提示使用者確認此動作。</span><span class="sxs-lookup"><span data-stu-id="e2269-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="e2269-111">範例2：移除網路介面</span><span class="sxs-lookup"><span data-stu-id="e2269-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzNetworkInterface -Force
```

<span data-ttu-id="e2269-112">這個命令會移除 [資源群組 ResourceGroup1] 中的所有網路介面。</span><span class="sxs-lookup"><span data-stu-id="e2269-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="e2269-113">因為使用 *Force* 參數，系統不會提示使用者確認。</span><span class="sxs-lookup"><span data-stu-id="e2269-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="e2269-114">參數</span><span class="sxs-lookup"><span data-stu-id="e2269-114">PARAMETERS</span></span>

### <span data-ttu-id="e2269-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2269-115">-AsJob</span></span>
<span data-ttu-id="e2269-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e2269-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2269-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2269-117">-DefaultProfile</span></span>
<span data-ttu-id="e2269-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e2269-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2269-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e2269-119">-Force</span></span>
<span data-ttu-id="e2269-120">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="e2269-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e2269-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e2269-121">-Name</span></span>
<span data-ttu-id="e2269-122">指定此 Cmdlet 移除之網路介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2269-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e2269-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2269-123">-PassThru</span></span>
<span data-ttu-id="e2269-124">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="e2269-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e2269-125">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="e2269-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e2269-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2269-126">-ResourceGroupName</span></span>
<span data-ttu-id="e2269-127">指定包含此 Cmdlet 移除之網路介面之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2269-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e2269-128">-確認</span><span class="sxs-lookup"><span data-stu-id="e2269-128">-Confirm</span></span>
<span data-ttu-id="e2269-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e2269-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2269-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2269-130">-WhatIf</span></span>
<span data-ttu-id="e2269-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e2269-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2269-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e2269-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2269-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2269-133">CommonParameters</span></span>
<span data-ttu-id="e2269-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e2269-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2269-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e2269-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2269-136">輸入</span><span class="sxs-lookup"><span data-stu-id="e2269-136">INPUTS</span></span>

### <span data-ttu-id="e2269-137">System.object</span><span class="sxs-lookup"><span data-stu-id="e2269-137">System.String</span></span>

## <span data-ttu-id="e2269-138">輸出</span><span class="sxs-lookup"><span data-stu-id="e2269-138">OUTPUTS</span></span>

### <span data-ttu-id="e2269-139">System.object</span><span class="sxs-lookup"><span data-stu-id="e2269-139">System.Boolean</span></span>

## <span data-ttu-id="e2269-140">筆記</span><span class="sxs-lookup"><span data-stu-id="e2269-140">NOTES</span></span>

## <span data-ttu-id="e2269-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="e2269-141">RELATED LINKS</span></span>

[<span data-ttu-id="e2269-142">AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e2269-142">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="e2269-143">新-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e2269-143">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="e2269-144">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e2269-144">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)



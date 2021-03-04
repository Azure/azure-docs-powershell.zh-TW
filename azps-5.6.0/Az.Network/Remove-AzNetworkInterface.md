---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
ms.openlocfilehash: 54bc4a3b9875f68df8a7c824c7e4f754e6f35a4e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912666"
---
# <span data-ttu-id="d6243-101">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d6243-101">Remove-AzNetworkInterface</span></span>

## <span data-ttu-id="d6243-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d6243-102">SYNOPSIS</span></span>
<span data-ttu-id="d6243-103">移除網路介面。</span><span class="sxs-lookup"><span data-stu-id="d6243-103">Removes a network interface.</span></span>

## <span data-ttu-id="d6243-104">語法</span><span class="sxs-lookup"><span data-stu-id="d6243-104">SYNTAX</span></span>

```
Remove-AzNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6243-105">描述</span><span class="sxs-lookup"><span data-stu-id="d6243-105">DESCRIPTION</span></span>
<span data-ttu-id="d6243-106">**Remove-AzNetworkInterface** Cmdlet 會移除 Azure 網路介面。</span><span class="sxs-lookup"><span data-stu-id="d6243-106">The **Remove-AzNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="d6243-107">例子</span><span class="sxs-lookup"><span data-stu-id="d6243-107">EXAMPLES</span></span>

### <span data-ttu-id="d6243-108">範例 1：移除網路介面</span><span class="sxs-lookup"><span data-stu-id="d6243-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="d6243-109">此命令會移除資源群組 ResourceGroup1 中的網路介面 NetworkInterface1。</span><span class="sxs-lookup"><span data-stu-id="d6243-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="d6243-110">由於 *不會使用 Force* 參數，因此系統會提示使用者確認此動作。</span><span class="sxs-lookup"><span data-stu-id="d6243-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="d6243-111">範例 2：移除網路介面</span><span class="sxs-lookup"><span data-stu-id="d6243-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzNetworkInterface -Force
```

<span data-ttu-id="d6243-112">此命令會移除資源群組 ResourceGroup1 中所有的網路介面。</span><span class="sxs-lookup"><span data-stu-id="d6243-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="d6243-113">由於 *使用 Force* 參數，因此系統不會提示使用者確認。</span><span class="sxs-lookup"><span data-stu-id="d6243-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="d6243-114">參數</span><span class="sxs-lookup"><span data-stu-id="d6243-114">PARAMETERS</span></span>

### <span data-ttu-id="d6243-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6243-115">-AsJob</span></span>
<span data-ttu-id="d6243-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d6243-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6243-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6243-117">-DefaultProfile</span></span>
<span data-ttu-id="d6243-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d6243-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6243-119">-強制</span><span class="sxs-lookup"><span data-stu-id="d6243-119">-Force</span></span>
<span data-ttu-id="d6243-120">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="d6243-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d6243-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d6243-121">-Name</span></span>
<span data-ttu-id="d6243-122">指定此 Cmdlet 移除的網路介面名稱。</span><span class="sxs-lookup"><span data-stu-id="d6243-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d6243-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6243-123">-PassThru</span></span>
<span data-ttu-id="d6243-124">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="d6243-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d6243-125">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="d6243-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d6243-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6243-126">-ResourceGroupName</span></span>
<span data-ttu-id="d6243-127">指定包含此 Cmdlet 移除之網路介面的資源組名。</span><span class="sxs-lookup"><span data-stu-id="d6243-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d6243-128">-確認</span><span class="sxs-lookup"><span data-stu-id="d6243-128">-Confirm</span></span>
<span data-ttu-id="d6243-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d6243-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6243-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6243-130">-WhatIf</span></span>
<span data-ttu-id="d6243-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d6243-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6243-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d6243-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6243-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6243-133">CommonParameters</span></span>
<span data-ttu-id="d6243-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d6243-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6243-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d6243-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6243-136">輸入</span><span class="sxs-lookup"><span data-stu-id="d6243-136">INPUTS</span></span>

### <span data-ttu-id="d6243-137">System.String</span><span class="sxs-lookup"><span data-stu-id="d6243-137">System.String</span></span>

## <span data-ttu-id="d6243-138">輸出</span><span class="sxs-lookup"><span data-stu-id="d6243-138">OUTPUTS</span></span>

### <span data-ttu-id="d6243-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d6243-139">System.Boolean</span></span>

## <span data-ttu-id="d6243-140">筆記</span><span class="sxs-lookup"><span data-stu-id="d6243-140">NOTES</span></span>

## <span data-ttu-id="d6243-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="d6243-141">RELATED LINKS</span></span>

[<span data-ttu-id="d6243-142">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d6243-142">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="d6243-143">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d6243-143">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="d6243-144">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d6243-144">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)



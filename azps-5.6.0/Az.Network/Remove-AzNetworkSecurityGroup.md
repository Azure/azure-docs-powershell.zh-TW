---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
ms.openlocfilehash: 27822e64c697ace3a69e6faf5f291215a2d89935
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912661"
---
# <span data-ttu-id="51916-101">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="51916-101">Remove-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="51916-102">簡介</span><span class="sxs-lookup"><span data-stu-id="51916-102">SYNOPSIS</span></span>
<span data-ttu-id="51916-103">移除網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="51916-103">Removes a network security group.</span></span>

## <span data-ttu-id="51916-104">語法</span><span class="sxs-lookup"><span data-stu-id="51916-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51916-105">描述</span><span class="sxs-lookup"><span data-stu-id="51916-105">DESCRIPTION</span></span>
<span data-ttu-id="51916-106">**Remove-AzNetworkSecurityGroup** Cmdlet 會移除 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="51916-106">The **Remove-AzNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="51916-107">例子</span><span class="sxs-lookup"><span data-stu-id="51916-107">EXAMPLES</span></span>

### <span data-ttu-id="51916-108">範例 1：移除網路安全性群組</span><span class="sxs-lookup"><span data-stu-id="51916-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="51916-109">此命令會移除名為 testRG NSG-FrontEnd資源群組中名為 "測試RG" 的安全性群組。</span><span class="sxs-lookup"><span data-stu-id="51916-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="51916-110">參數</span><span class="sxs-lookup"><span data-stu-id="51916-110">PARAMETERS</span></span>

### <span data-ttu-id="51916-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51916-111">-AsJob</span></span>
<span data-ttu-id="51916-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="51916-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51916-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51916-113">-DefaultProfile</span></span>
<span data-ttu-id="51916-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="51916-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51916-115">-強制</span><span class="sxs-lookup"><span data-stu-id="51916-115">-Force</span></span>
<span data-ttu-id="51916-116">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="51916-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="51916-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="51916-117">-Name</span></span>
<span data-ttu-id="51916-118">指定此 Cmdlet 移除的網路安全性群組名。</span><span class="sxs-lookup"><span data-stu-id="51916-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="51916-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51916-119">-PassThru</span></span>
<span data-ttu-id="51916-120">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="51916-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="51916-121">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="51916-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="51916-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51916-122">-ResourceGroupName</span></span>
<span data-ttu-id="51916-123">指定此 Cmdlet 移除網路安全性群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="51916-123">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

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

### <span data-ttu-id="51916-124">-確認</span><span class="sxs-lookup"><span data-stu-id="51916-124">-Confirm</span></span>
<span data-ttu-id="51916-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="51916-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51916-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51916-126">-WhatIf</span></span>
<span data-ttu-id="51916-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="51916-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51916-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="51916-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51916-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51916-129">CommonParameters</span></span>
<span data-ttu-id="51916-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="51916-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51916-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="51916-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51916-132">輸入</span><span class="sxs-lookup"><span data-stu-id="51916-132">INPUTS</span></span>

### <span data-ttu-id="51916-133">System.String</span><span class="sxs-lookup"><span data-stu-id="51916-133">System.String</span></span>

## <span data-ttu-id="51916-134">輸出</span><span class="sxs-lookup"><span data-stu-id="51916-134">OUTPUTS</span></span>

### <span data-ttu-id="51916-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="51916-135">System.Boolean</span></span>

## <span data-ttu-id="51916-136">筆記</span><span class="sxs-lookup"><span data-stu-id="51916-136">NOTES</span></span>

## <span data-ttu-id="51916-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="51916-137">RELATED LINKS</span></span>

[<span data-ttu-id="51916-138">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="51916-138">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="51916-139">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="51916-139">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="51916-140">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="51916-140">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)



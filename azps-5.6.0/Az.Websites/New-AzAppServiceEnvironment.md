---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azappserviceenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironment.md
ms.openlocfilehash: a922958ec2e15ea9cb4a3b0189f74dda6d71eab2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916818"
---
# <span data-ttu-id="79406-101">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="79406-101">New-AzAppServiceEnvironment</span></span>

## <span data-ttu-id="79406-102">簡介</span><span class="sxs-lookup"><span data-stu-id="79406-102">SYNOPSIS</span></span>
<span data-ttu-id="79406-103">建立 App 服務環境，包括建議的路由資料表和網路安全性群組</span><span class="sxs-lookup"><span data-stu-id="79406-103">Creates an App Service Environment including the recommended Route Table and Network Security Group</span></span>

## <span data-ttu-id="79406-104">語法</span><span class="sxs-lookup"><span data-stu-id="79406-104">SYNTAX</span></span>

### <span data-ttu-id="79406-105">ASEv2SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="79406-105">ASEv2SubnetNameParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -VirtualNetworkName <String> -SubnetName <String> -LoadBalancerMode <String>
 [-SkipRouteTable] [-SkipNetworkSecurityGroup] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79406-106">ASEv3SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="79406-106">ASEv3SubnetNameParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -VirtualNetworkName <String> -SubnetName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79406-107">ASEv2SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="79406-107">ASEv2SubnetIdParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -SubnetId <String> -LoadBalancerMode <String> [-SkipRouteTable] [-SkipNetworkSecurityGroup]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79406-108">ASEv3SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="79406-108">ASEv3SubnetIdParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -SubnetId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79406-109">描述</span><span class="sxs-lookup"><span data-stu-id="79406-109">DESCRIPTION</span></span>
<span data-ttu-id="79406-110">**New-AzAppServiceEnvironment** Cmdlet 會建立應用程式服務環境。</span><span class="sxs-lookup"><span data-stu-id="79406-110">The **New-AzAppServiceEnvironment** cmdlet creates an App Service Environment.</span></span>

## <span data-ttu-id="79406-111">例子</span><span class="sxs-lookup"><span data-stu-id="79406-111">EXAMPLES</span></span>

### <span data-ttu-id="79406-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="79406-112">Example 1</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseV2 -Location WestEurope 
        -VirtualNetworkName MyVirtualNetwork -SubnetName AseSubnet -LoadBalancerMode Internal
```

<span data-ttu-id="79406-113">建立名為 MyAseV2 的應用程式服務環境，包括建議的路由資料表和網路安全性群組</span><span class="sxs-lookup"><span data-stu-id="79406-113">Create App Service Environment named MyAseV2 including recommended Route Table and Network Security Group</span></span>

### <span data-ttu-id="79406-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="79406-114">Example 2</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseV2 -Location WestEurope 
        -VirtualNetworkName MyVirtualNetwork -SubnetName AseSubnet -LoadBalancerMode Internal
        -SkipRouteTable -SkipNetworkSecurityGroup
```

<span data-ttu-id="79406-115">建立名為 MyAseV2 的應用程式服務環境，但不建議路由資料表和網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="79406-115">Create App Service Environment named MyAseV2 without recommended Route Table and Network Security Group.</span></span>
<span data-ttu-id="79406-116">這些應該先于提供應用程式服務環境之前或之後建立，以確保功能實例。</span><span class="sxs-lookup"><span data-stu-id="79406-116">These should be create before or right after provisioning the App Service Environment to ensure a functional instance.</span></span>

## <span data-ttu-id="79406-117">參數</span><span class="sxs-lookup"><span data-stu-id="79406-117">PARAMETERS</span></span>

### <span data-ttu-id="79406-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79406-118">-AsJob</span></span>
<span data-ttu-id="79406-119">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="79406-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="79406-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79406-120">-DefaultProfile</span></span>
<span data-ttu-id="79406-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="79406-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79406-122">-Kind</span><span class="sxs-lookup"><span data-stu-id="79406-122">-Kind</span></span>
<span data-ttu-id="79406-123">應用程式服務環境的版本。</span><span class="sxs-lookup"><span data-stu-id="79406-123">The version of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ASEv2, ASEv3

Required: False
Position: 3
Default value: ASEv2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79406-124">-LoadBalancerMode</span><span class="sxs-lookup"><span data-stu-id="79406-124">-LoadBalancerMode</span></span>
<span data-ttu-id="79406-125">應用程式服務環境的負載平衡器模式。</span><span class="sxs-lookup"><span data-stu-id="79406-125">Load balancer mode of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv2SubnetIdParameterSet
Aliases:
Accepted values: Internal, External

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79406-126">-位置</span><span class="sxs-lookup"><span data-stu-id="79406-126">-Location</span></span>
<span data-ttu-id="79406-127">應用程式服務環境的位置，例如：西歐。</span><span class="sxs-lookup"><span data-stu-id="79406-127">The Location of the app service environment eg: West Europe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79406-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="79406-128">-Name</span></span>
<span data-ttu-id="79406-129">應用程式服務環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="79406-129">The name of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79406-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79406-130">-PassThru</span></span>
<span data-ttu-id="79406-131">返回應用程式服務環境物件。</span><span class="sxs-lookup"><span data-stu-id="79406-131">Return the app service environment object.</span></span>

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

### <span data-ttu-id="79406-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79406-132">-ResourceGroupName</span></span>
<span data-ttu-id="79406-133">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="79406-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79406-134">-SkipNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="79406-134">-SkipNetworkSecurityGroup</span></span>
<span data-ttu-id="79406-135">請勿在應用程式服務環境中建立建議的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="79406-135">Do not create the recommended network security group as part of the app service environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv2SubnetIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79406-136">-SkipRouteTable</span><span class="sxs-lookup"><span data-stu-id="79406-136">-SkipRouteTable</span></span>
<span data-ttu-id="79406-137">請勿建立建議路由資料表做為應用程式服務環境的一部分。</span><span class="sxs-lookup"><span data-stu-id="79406-137">Do not create the recommended route table as part of the app service environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv2SubnetIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79406-138">-子網Id</span><span class="sxs-lookup"><span data-stu-id="79406-138">-SubnetId</span></span>
<span data-ttu-id="79406-139">子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="79406-139">The subnet id.</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetIdParameterSet, ASEv3SubnetIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79406-140">-子網名稱</span><span class="sxs-lookup"><span data-stu-id="79406-140">-SubnetName</span></span>
<span data-ttu-id="79406-141">子網名稱。</span><span class="sxs-lookup"><span data-stu-id="79406-141">The subnet name.</span></span> <span data-ttu-id="79406-142">與 -VirtualNetworkName 搭配使用，且必須和 ASE 在同一個資源群組中。</span><span class="sxs-lookup"><span data-stu-id="79406-142">Used in combination with -VirtualNetworkName and must be in same resource group as ASE.</span></span> <span data-ttu-id="79406-143">如果沒有，請使用 -子網Id</span><span class="sxs-lookup"><span data-stu-id="79406-143">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv3SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79406-144">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="79406-144">-VirtualNetworkName</span></span>
<span data-ttu-id="79406-145">vNet 名稱。</span><span class="sxs-lookup"><span data-stu-id="79406-145">The vNet name.</span></span> <span data-ttu-id="79406-146">與 -子網名稱搭配使用，且必須和 ASE 在同一個資源群組中。</span><span class="sxs-lookup"><span data-stu-id="79406-146">Used in combination with -SubnetName and must be in same resource group as ASE.</span></span> <span data-ttu-id="79406-147">如果沒有，請使用 -子網Id</span><span class="sxs-lookup"><span data-stu-id="79406-147">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv3SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79406-148">-確認</span><span class="sxs-lookup"><span data-stu-id="79406-148">-Confirm</span></span>
<span data-ttu-id="79406-149">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="79406-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79406-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79406-150">-WhatIf</span></span>
<span data-ttu-id="79406-151">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="79406-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79406-152">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="79406-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79406-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79406-153">CommonParameters</span></span>
<span data-ttu-id="79406-154">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="79406-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79406-155">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79406-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79406-156">輸入</span><span class="sxs-lookup"><span data-stu-id="79406-156">INPUTS</span></span>

### <span data-ttu-id="79406-157">沒有</span><span class="sxs-lookup"><span data-stu-id="79406-157">None</span></span>

## <span data-ttu-id="79406-158">輸出</span><span class="sxs-lookup"><span data-stu-id="79406-158">OUTPUTS</span></span>

### <span data-ttu-id="79406-159">System.Object</span><span class="sxs-lookup"><span data-stu-id="79406-159">System.Object</span></span>
## <span data-ttu-id="79406-160">筆記</span><span class="sxs-lookup"><span data-stu-id="79406-160">NOTES</span></span>

## <span data-ttu-id="79406-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="79406-161">RELATED LINKS</span></span>

[<span data-ttu-id="79406-162">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="79406-162">Get-AzAppServiceEnvironment</span></span>](./Get-AzAppServiceEnvironment.md)

[<span data-ttu-id="79406-163">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="79406-163">New-AzAppServiceEnvironmentInboundServices</span></span>](./New-AzAppServiceEnvironmentInboundServices.md)

[<span data-ttu-id="79406-164">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="79406-164">Remove-AzAppServiceEnvironment</span></span>](./Remove-AzAppServiceEnvironment.md)

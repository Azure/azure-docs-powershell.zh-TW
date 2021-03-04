---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azappserviceenvironmentinboundservices
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironmentInboundServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironmentInboundServices.md
ms.openlocfilehash: 68b2957e959365187ad82980bd2be2f055632a57
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914982"
---
# <span data-ttu-id="1ad30-101">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="1ad30-101">New-AzAppServiceEnvironmentInboundServices</span></span>

## <span data-ttu-id="1ad30-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1ad30-102">SYNOPSIS</span></span>
<span data-ttu-id="1ad30-103">為應用程式服務環境建立內入服務。</span><span class="sxs-lookup"><span data-stu-id="1ad30-103">Creates inbound services for App Service Environment.</span></span> <span data-ttu-id="1ad30-104">針對 ASEv2 ILB，這會建立 Azure 專用 DNS 區域及記錄以與內部 IP 進行地圖。</span><span class="sxs-lookup"><span data-stu-id="1ad30-104">For ASEv2 ILB, this will create an Azure Private DNS Zone and records to map to the internal IP.</span></span> <span data-ttu-id="1ad30-105">此外，ASEv3 也會確保子網已停用網路原則，並且會建立私人端點。</span><span class="sxs-lookup"><span data-stu-id="1ad30-105">For ASEv3 it will in addition ensure subnet has Network Policy disabled and will create a private endpoint.</span></span>

## <span data-ttu-id="1ad30-106">語法</span><span class="sxs-lookup"><span data-stu-id="1ad30-106">SYNTAX</span></span>

### <span data-ttu-id="1ad30-107">子網名稱ParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ad30-107">SubnetNameParameterSet</span></span>
```
New-AzAppServiceEnvironmentInboundServices [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkName <String> -SubnetName <String> [-SkipDns] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ad30-108">子網IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ad30-108">SubnetIdParameterSet</span></span>
```
New-AzAppServiceEnvironmentInboundServices [-ResourceGroupName] <String> [-Name] <String> -SubnetId <String>
 [-SkipDns] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ad30-109">描述</span><span class="sxs-lookup"><span data-stu-id="1ad30-109">DESCRIPTION</span></span>
<span data-ttu-id="1ad30-110">**New-AzAppServiceEnvironmentInboundServices** Cmdlet 會為應用程式服務環境建立內建服務。</span><span class="sxs-lookup"><span data-stu-id="1ad30-110">The **New-AzAppServiceEnvironmentInboundServices** cmdlet create inbound services for an App Service Environment.</span></span>

## <span data-ttu-id="1ad30-111">例子</span><span class="sxs-lookup"><span data-stu-id="1ad30-111">EXAMPLES</span></span>

### <span data-ttu-id="1ad30-112">範例 1：建立 ASEv2 的專用 DNS 區域與記錄</span><span class="sxs-lookup"><span data-stu-id="1ad30-112">Example 1: Create Private DNS Zone and records for ASEv2</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironmentInboundServices -ResourceGroupName AseResourceGroup -Name AseV2Name
-VirtualNetworkName MyVirtualNetwork -SubnetName InboundSubnet
```

<span data-ttu-id="1ad30-113">建立 ASEv2 的專用 DNS 區域與記錄</span><span class="sxs-lookup"><span data-stu-id="1ad30-113">Create Private DNS Zone and records for ASEv2</span></span>

### <span data-ttu-id="1ad30-114">範例 2：建立 ASEv3 的專用端點、私人 DNS 區域及記錄</span><span class="sxs-lookup"><span data-stu-id="1ad30-114">Example 2: Create private endpoint, Private DNS Zone and records for ASEv3</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironmentInboundServices -ResourceGroupName AseResourceGroup -Name AseV2Name
-VirtualNetworkName MyVirtualNetwork -SubnetName InboundSubnet
```

<span data-ttu-id="1ad30-115">為 ASEv3 建立私人端點、私人 DNS 區域及記錄</span><span class="sxs-lookup"><span data-stu-id="1ad30-115">Create private endpoint, Private DNS Zone and records for ASEv3</span></span>

### <span data-ttu-id="1ad30-116">範例 3：建立 ASEv3 的私人端點</span><span class="sxs-lookup"><span data-stu-id="1ad30-116">Example 3: Create private endpoint for ASEv3</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironmentInboundServices -ResourceGroupName AseResourceGroup -Name AseV2Name
-VirtualNetworkName MyVirtualNetwork -SubnetName InboundSubnet -SkipDns
```

<span data-ttu-id="1ad30-117">建立 ASEv3 的私人端點</span><span class="sxs-lookup"><span data-stu-id="1ad30-117">Create private endpoint for ASEv3</span></span>

## <span data-ttu-id="1ad30-118">參數</span><span class="sxs-lookup"><span data-stu-id="1ad30-118">PARAMETERS</span></span>

### <span data-ttu-id="1ad30-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ad30-119">-DefaultProfile</span></span>
<span data-ttu-id="1ad30-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1ad30-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ad30-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="1ad30-121">-Name</span></span>
<span data-ttu-id="1ad30-122">應用程式服務環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ad30-122">The name of the app service environment.</span></span>

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

### <span data-ttu-id="1ad30-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ad30-123">-PassThru</span></span>
<span data-ttu-id="1ad30-124">退貨狀態。</span><span class="sxs-lookup"><span data-stu-id="1ad30-124">Return status.</span></span>

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

### <span data-ttu-id="1ad30-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ad30-125">-ResourceGroupName</span></span>
<span data-ttu-id="1ad30-126">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ad30-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="1ad30-127">-SkipDns</span><span class="sxs-lookup"><span data-stu-id="1ad30-127">-SkipDns</span></span>
<span data-ttu-id="1ad30-128">請勿建立 Azure 私人 DNS 區域及記錄。</span><span class="sxs-lookup"><span data-stu-id="1ad30-128">Do not create Azure Private DNS Zone and records.</span></span>

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

### <span data-ttu-id="1ad30-129">-子網Id</span><span class="sxs-lookup"><span data-stu-id="1ad30-129">-SubnetId</span></span>
<span data-ttu-id="1ad30-130">子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="1ad30-130">The subnet id.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ad30-131">-子網名稱</span><span class="sxs-lookup"><span data-stu-id="1ad30-131">-SubnetName</span></span>
<span data-ttu-id="1ad30-132">子網名稱。</span><span class="sxs-lookup"><span data-stu-id="1ad30-132">The subnet name.</span></span> <span data-ttu-id="1ad30-133">與 -VirtualNetworkName 搭配使用，且必須和 ASE 在同一個資源群組中。</span><span class="sxs-lookup"><span data-stu-id="1ad30-133">Used in combination with -VirtualNetworkName and must be in same resource group as ASE.</span></span> <span data-ttu-id="1ad30-134">如果沒有，請使用 -子網Id</span><span class="sxs-lookup"><span data-stu-id="1ad30-134">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ad30-135">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="1ad30-135">-VirtualNetworkName</span></span>
<span data-ttu-id="1ad30-136">vNet 名稱。</span><span class="sxs-lookup"><span data-stu-id="1ad30-136">The vNet name.</span></span> <span data-ttu-id="1ad30-137">與 -子網名稱搭配使用，且必須和 ASE 在同一個資源群組中。</span><span class="sxs-lookup"><span data-stu-id="1ad30-137">Used in combination with -SubnetName and must be in same resource group as ASE.</span></span> <span data-ttu-id="1ad30-138">如果沒有，請使用 -子網Id</span><span class="sxs-lookup"><span data-stu-id="1ad30-138">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ad30-139">-確認</span><span class="sxs-lookup"><span data-stu-id="1ad30-139">-Confirm</span></span>
<span data-ttu-id="1ad30-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1ad30-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ad30-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ad30-141">-WhatIf</span></span>
<span data-ttu-id="1ad30-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1ad30-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ad30-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1ad30-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ad30-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ad30-144">CommonParameters</span></span>
<span data-ttu-id="1ad30-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1ad30-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ad30-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ad30-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ad30-147">輸入</span><span class="sxs-lookup"><span data-stu-id="1ad30-147">INPUTS</span></span>

### <span data-ttu-id="1ad30-148">沒有</span><span class="sxs-lookup"><span data-stu-id="1ad30-148">None</span></span>

## <span data-ttu-id="1ad30-149">輸出</span><span class="sxs-lookup"><span data-stu-id="1ad30-149">OUTPUTS</span></span>

### <span data-ttu-id="1ad30-150">System.Object</span><span class="sxs-lookup"><span data-stu-id="1ad30-150">System.Object</span></span>
## <span data-ttu-id="1ad30-151">筆記</span><span class="sxs-lookup"><span data-stu-id="1ad30-151">NOTES</span></span>

## <span data-ttu-id="1ad30-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ad30-152">RELATED LINKS</span></span>

[<span data-ttu-id="1ad30-153">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="1ad30-153">New-AzAppServiceEnvironment</span></span>](./New-AzAppServiceEnvironment.md)

[<span data-ttu-id="1ad30-154">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="1ad30-154">Get-AzAppServiceEnvironment</span></span>](./Get-AzAppServiceEnvironment.md)

[<span data-ttu-id="1ad30-155">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="1ad30-155">Remove-AzAppServiceEnvironment</span></span>](./Remove-AzAppServiceEnvironment.md)
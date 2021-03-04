---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: b28cb8ac408ff281930eac68bf2b97d288150dd6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909906"
---
# <span data-ttu-id="90c59-101">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="90c59-101">Add-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="90c59-102">簡介</span><span class="sxs-lookup"><span data-stu-id="90c59-102">SYNOPSIS</span></span>
<span data-ttu-id="90c59-103">新增 Access Restiction 規則至 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="90c59-103">Adds an Access Restiction rule to an Azure Web App.</span></span>

## <span data-ttu-id="90c59-104">語法</span><span class="sxs-lookup"><span data-stu-id="90c59-104">SYNTAX</span></span>

### <span data-ttu-id="90c59-105">IpAddressParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="90c59-105">IpAddressParameterSet (Default)</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -IpAddress <String> [-PassThru] [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90c59-106">ServiceTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="90c59-106">ServiceTagParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 [-PassThru] -ServiceTag <String> [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90c59-107">子網名稱ParameterSet</span><span class="sxs-lookup"><span data-stu-id="90c59-107">SubnetNameParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetName <String> -VirtualNetworkName <String> [-IgnoreMissingServiceEndpoint] [-PassThru]
 [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90c59-108">子網IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="90c59-108">SubnetIdParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetId <String> [-IgnoreMissingServiceEndpoint] [-PassThru] [-HttpHeader <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90c59-109">描述</span><span class="sxs-lookup"><span data-stu-id="90c59-109">DESCRIPTION</span></span>
<span data-ttu-id="90c59-110">**Add-AzWebAppAccessRestrictionRule** Cmdlet 會新增存取限制規則至 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="90c59-110">The **Add-AzWebAppAccessRestrictionRule** cmdlet adds an Access Restriction rule to an Azure Web App.</span></span>

## <span data-ttu-id="90c59-111">例子</span><span class="sxs-lookup"><span data-stu-id="90c59-111">EXAMPLES</span></span>

### <span data-ttu-id="90c59-112">範例 1：新增 IpAddress Access 限制規則至 Web App</span><span class="sxs-lookup"><span data-stu-id="90c59-112">Example 1: Add IpAddress Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name IpRule -Priority 200 -Action Allow -IpAddress 10.10.0.0/8
```

<span data-ttu-id="90c59-113">此命令會將優先順序為 200 和 ip 範圍的存取限制規則新增到屬於資源群組 Default-Web-WestUS 的名為 ContosoSite 的 Web App。</span><span class="sxs-lookup"><span data-stu-id="90c59-113">This command adds an access restriction rule with priority 200 and ip range to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="90c59-114">範例 2：新增子網服務端點存取限制規則至 Web App</span><span class="sxs-lookup"><span data-stu-id="90c59-114">Example 2: Add Subnet Service Endpoint Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name SubnetRule -Priority 300 -Action Allow -SubnetName appgw-subnet -VirtualNetworkName corp-vnet
```

<span data-ttu-id="90c59-115">此命令會將優先順序為 300 且具有 corp-vnet 子網 appgw-子網的存取限制規則新增到屬於資源群組 Default-Web-WestUS 的 Web App，名為 ContosoSite。</span><span class="sxs-lookup"><span data-stu-id="90c59-115">This command adds an access restriction rule with priority 300 and with subnet appgw-subnet in corp-vnet to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="90c59-116">範例 3：新增 ServiceTag 存取限制規則至 Web App</span><span class="sxs-lookup"><span data-stu-id="90c59-116">Example 3: Add ServiceTag Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name ServiceTagRule -Priority 200 -Action Allow -ServiceTag AzureFrontDoor.Backend
```

<span data-ttu-id="90c59-117">此命令會將優先順序為 200 的存取限制規則，以及代表 Azure Front Door ip 範圍的服務標籤新增到屬於資源群組 Default-Web-WestUS 的 ContosoSite Web App。</span><span class="sxs-lookup"><span data-stu-id="90c59-117">This command adds an access restriction rule with priority 200 and a Service Tag representing the ip scope of Azure Front Door to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="90c59-118">範例 4：新增多重位址存取限制規則至 Web App</span><span class="sxs-lookup"><span data-stu-id="90c59-118">Example 4: Add multi-address Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name MultipleIpRule -Priority 200 -Action Allow -IpAddress "10.10.0.0/8,192.168.0.0/16"
```

<span data-ttu-id="90c59-119">此命令會將優先順序為 200 和兩個 ip 範圍的存取限制規則新增到屬於資源群組 Default-Web-WestUS 的名為 ContosoSite 的 Web App。</span><span class="sxs-lookup"><span data-stu-id="90c59-119">This command adds an access restriction rule with priority 200 and two ip ranges to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="90c59-120">範例 5：新增具有 HTTP 標頭的存取限制規則至 Web App</span><span class="sxs-lookup"><span data-stu-id="90c59-120">Example 5: Add Access Restriction rule with http header to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name MultipleIpRule -Priority 400 -Action Allow -ServiceTag AzureFrontDoor.Backend
-HttpHeader @{'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'; 'x-azure-fdid' = '355deb06-47c4-4ba4-9641-c7d7a98b913e'}
```

<span data-ttu-id="90c59-121">此命令會針對服務標記 AzureFrontDoor.後端新增優先順序為 400 的存取限制規則，進一步限制對屬於資源群組 Default-Web-WestUS 的 Web App 存取特定值的 HTTP 標頭。</span><span class="sxs-lookup"><span data-stu-id="90c59-121">This command adds an access restriction rule with priority 400 for Service Tag AzureFrontDoor.Backend and further restricts access only to http headers of certain values to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="90c59-122">參數</span><span class="sxs-lookup"><span data-stu-id="90c59-122">PARAMETERS</span></span>

### <span data-ttu-id="90c59-123">-動作</span><span class="sxs-lookup"><span data-stu-id="90c59-123">-Action</span></span>
<span data-ttu-id="90c59-124">允許或拒絕規則。</span><span class="sxs-lookup"><span data-stu-id="90c59-124">Allow or Deny rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: Allow
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c59-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90c59-125">-DefaultProfile</span></span>
<span data-ttu-id="90c59-126">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="90c59-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90c59-127">-描述</span><span class="sxs-lookup"><span data-stu-id="90c59-127">-Description</span></span>
<span data-ttu-id="90c59-128">存取限制描述。</span><span class="sxs-lookup"><span data-stu-id="90c59-128">Access Restriction description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c59-129">-HTTPHeader</span><span class="sxs-lookup"><span data-stu-id="90c59-129">-HttpHeader</span></span>
<span data-ttu-id="90c59-130">HTTP 標頭限制。</span><span class="sxs-lookup"><span data-stu-id="90c59-130">Http header restrictions.</span></span> <span data-ttu-id="90c59-131">範例：-HTTPHeader @{'x-azure-fdid' = '7acacb02-47ea-4cd4-b568-5e880e72582e';'x-forwarded-host' = 'www.contoso.com'， 'app.contoso.com'}</span><span class="sxs-lookup"><span data-stu-id="90c59-131">Example: -HttpHeader @{'x-azure-fdid' = '7acacb02-47ea-4cd4-b568-5e880e72582e'; 'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c59-132">-IgnoreMissingServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="90c59-132">-IgnoreMissingServiceEndpoint</span></span>
<span data-ttu-id="90c59-133">指定應驗證子網的服務端點註冊。</span><span class="sxs-lookup"><span data-stu-id="90c59-133">Specify if Service Endpoint registration at Subnet should be validated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SubnetNameParameterSet, SubnetIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c59-134">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="90c59-134">-IpAddress</span></span>
<span data-ttu-id="90c59-135">Ip Address v4 或 v6 CIDR 範圍。</span><span class="sxs-lookup"><span data-stu-id="90c59-135">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="90c59-136">例如：192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="90c59-136">E.g.: 192.168.0.0/24</span></span>

```yaml
Type: System.String
Parameter Sets: IpAddressParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c59-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="90c59-137">-Name</span></span>
<span data-ttu-id="90c59-138">規則名稱</span><span class="sxs-lookup"><span data-stu-id="90c59-138">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c59-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90c59-139">-PassThru</span></span>
<span data-ttu-id="90c59-140">返回存取限制 config 物件。</span><span class="sxs-lookup"><span data-stu-id="90c59-140">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="90c59-141">-優先順序</span><span class="sxs-lookup"><span data-stu-id="90c59-141">-Priority</span></span>
<span data-ttu-id="90c59-142">存取限制優先順序。</span><span class="sxs-lookup"><span data-stu-id="90c59-142">Access Restriction priority.</span></span> <span data-ttu-id="90c59-143">例如：500。</span><span class="sxs-lookup"><span data-stu-id="90c59-143">E.g.: 500.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c59-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90c59-144">-ResourceGroupName</span></span>
<span data-ttu-id="90c59-145">資源組名</span><span class="sxs-lookup"><span data-stu-id="90c59-145">Resource Group Name</span></span>

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

### <span data-ttu-id="90c59-146">-ServiceTag</span><span class="sxs-lookup"><span data-stu-id="90c59-146">-ServiceTag</span></span>
<span data-ttu-id="90c59-147">服務標記名稱</span><span class="sxs-lookup"><span data-stu-id="90c59-147">Name of Service Tag</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceTagParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c59-148">-SlotName</span><span class="sxs-lookup"><span data-stu-id="90c59-148">-SlotName</span></span>
<span data-ttu-id="90c59-149">部署插槽名稱。</span><span class="sxs-lookup"><span data-stu-id="90c59-149">Deployment Slot name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c59-150">-子網Id</span><span class="sxs-lookup"><span data-stu-id="90c59-150">-SubnetId</span></span>
<span data-ttu-id="90c59-151">子網的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="90c59-151">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="90c59-152">-子網名稱</span><span class="sxs-lookup"><span data-stu-id="90c59-152">-SubnetName</span></span>
<span data-ttu-id="90c59-153">子網名稱。</span><span class="sxs-lookup"><span data-stu-id="90c59-153">Name of Subnet.</span></span>

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

### <span data-ttu-id="90c59-154">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="90c59-154">-TargetScmSite</span></span>
<span data-ttu-id="90c59-155">規則適用于主要網站或 Scm 網站。</span><span class="sxs-lookup"><span data-stu-id="90c59-155">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="90c59-156">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="90c59-156">-VirtualNetworkName</span></span>
<span data-ttu-id="90c59-157">虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="90c59-157">Name of Virtual Network.</span></span>

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

### <span data-ttu-id="90c59-158">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="90c59-158">-WebAppName</span></span>
<span data-ttu-id="90c59-159">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="90c59-159">The name of the web app.</span></span>

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

### <span data-ttu-id="90c59-160">-確認</span><span class="sxs-lookup"><span data-stu-id="90c59-160">-Confirm</span></span>
<span data-ttu-id="90c59-161">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="90c59-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90c59-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90c59-162">-WhatIf</span></span>
<span data-ttu-id="90c59-163">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="90c59-163">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90c59-164">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90c59-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90c59-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90c59-165">CommonParameters</span></span>
<span data-ttu-id="90c59-166">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="90c59-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90c59-167">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90c59-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90c59-168">輸入</span><span class="sxs-lookup"><span data-stu-id="90c59-168">INPUTS</span></span>

### <span data-ttu-id="90c59-169">System.String</span><span class="sxs-lookup"><span data-stu-id="90c59-169">System.String</span></span>

## <span data-ttu-id="90c59-170">輸出</span><span class="sxs-lookup"><span data-stu-id="90c59-170">OUTPUTS</span></span>

### <span data-ttu-id="90c59-171">Microsoft.Azure.Commands.WebApps.models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="90c59-171">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="90c59-172">筆記</span><span class="sxs-lookup"><span data-stu-id="90c59-172">NOTES</span></span>

## <span data-ttu-id="90c59-173">相關連結</span><span class="sxs-lookup"><span data-stu-id="90c59-173">RELATED LINKS</span></span>

[<span data-ttu-id="90c59-174">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="90c59-174">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="90c59-175">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="90c59-175">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="90c59-176">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="90c59-176">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: b28cb8ac408ff281930eac68bf2b97d288150dd6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133375"
---
# <span data-ttu-id="cb935-101">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="cb935-101">Add-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="cb935-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb935-102">SYNOPSIS</span></span>
<span data-ttu-id="cb935-103">新增 Access Restiction 規則至 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="cb935-103">Adds an Access Restiction rule to an Azure Web App.</span></span>

## <span data-ttu-id="cb935-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb935-104">SYNTAX</span></span>

### <span data-ttu-id="cb935-105">IpAddressParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="cb935-105">IpAddressParameterSet (Default)</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -IpAddress <String> [-PassThru] [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb935-106">ServiceTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb935-106">ServiceTagParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 [-PassThru] -ServiceTag <String> [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb935-107">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb935-107">SubnetNameParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetName <String> -VirtualNetworkName <String> [-IgnoreMissingServiceEndpoint] [-PassThru]
 [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb935-108">SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb935-108">SubnetIdParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetId <String> [-IgnoreMissingServiceEndpoint] [-PassThru] [-HttpHeader <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb935-109">說明</span><span class="sxs-lookup"><span data-stu-id="cb935-109">DESCRIPTION</span></span>
<span data-ttu-id="cb935-110">**AzWebAppAccessRestrictionRule** Cmdlet 會將存取限制規則新增至 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="cb935-110">The **Add-AzWebAppAccessRestrictionRule** cmdlet adds an Access Restriction rule to an Azure Web App.</span></span>

## <span data-ttu-id="cb935-111">示例</span><span class="sxs-lookup"><span data-stu-id="cb935-111">EXAMPLES</span></span>

### <span data-ttu-id="cb935-112">範例1：將 IpAddress 存取限制規則新增至 Web App</span><span class="sxs-lookup"><span data-stu-id="cb935-112">Example 1: Add IpAddress Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name IpRule -Priority 200 -Action Allow -IpAddress 10.10.0.0/8
```

<span data-ttu-id="cb935-113">這個命令會將具有優先順序200和 ip 範圍的訪問限制規則新增到一個名為「ContosoSite」的 Web 應用程式，而該 App 屬於資源群組的 [預設-WestUS]。</span><span class="sxs-lookup"><span data-stu-id="cb935-113">This command adds an access restriction rule with priority 200 and ip range to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="cb935-114">範例2：新增子網服務端點存取限制規則至 Web App</span><span class="sxs-lookup"><span data-stu-id="cb935-114">Example 2: Add Subnet Service Endpoint Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name SubnetRule -Priority 300 -Action Allow -SubnetName appgw-subnet -VirtualNetworkName corp-vnet
```

<span data-ttu-id="cb935-115">這個命令會將優先順序為300的 access 限制規則，以及在 corp-vnet 中，將子網 appgw 子網與屬於資源群組 Default-WestUS 的 Web App。</span><span class="sxs-lookup"><span data-stu-id="cb935-115">This command adds an access restriction rule with priority 300 and with subnet appgw-subnet in corp-vnet to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="cb935-116">範例3：在 Web 應用程式中新增 ServiceTag 存取限制規則</span><span class="sxs-lookup"><span data-stu-id="cb935-116">Example 3: Add ServiceTag Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name ServiceTagRule -Priority 200 -Action Allow -ServiceTag AzureFrontDoor.Backend
```

<span data-ttu-id="cb935-117">這個命令會新增一個優先順序為200的 access 限制規則，並將代表 Azure 前門之 ip 範圍的服務標記，指向屬於資源群組 Default-Web-WestUS 的 Web App。</span><span class="sxs-lookup"><span data-stu-id="cb935-117">This command adds an access restriction rule with priority 200 and a Service Tag representing the ip scope of Azure Front Door to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="cb935-118">範例4：新增多位址存取限制規則至 Web App</span><span class="sxs-lookup"><span data-stu-id="cb935-118">Example 4: Add multi-address Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name MultipleIpRule -Priority 200 -Action Allow -IpAddress "10.10.0.0/8,192.168.0.0/16"
```

<span data-ttu-id="cb935-119">這個命令會將具有優先順序200和兩個 ip 範圍的訪問限制規則新增到一個名為「ContosoSite」的 Web App，而該應用程式屬於資源群組的 Default-Web WestUS。</span><span class="sxs-lookup"><span data-stu-id="cb935-119">This command adds an access restriction rule with priority 200 and two ip ranges to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="cb935-120">範例5：在 Web 應用程式中新增含 HTTP 標頭的 Access 限制規則</span><span class="sxs-lookup"><span data-stu-id="cb935-120">Example 5: Add Access Restriction rule with http header to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name MultipleIpRule -Priority 400 -Action Allow -ServiceTag AzureFrontDoor.Backend
-HttpHeader @{'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'; 'x-azure-fdid' = '355deb06-47c4-4ba4-9641-c7d7a98b913e'}
```

<span data-ttu-id="cb935-121">這個命令會新增具有優先順序400（針對 Service 標記 AzureFrontDoor）的訪問限制規則，並進一步限制只存取特定值的 HTTP 標頭至屬於資源群組的 Web 應用程式（預設為 [Web-WestUS]）。</span><span class="sxs-lookup"><span data-stu-id="cb935-121">This command adds an access restriction rule with priority 400 for Service Tag AzureFrontDoor.Backend and further restricts access only to http headers of certain values to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="cb935-122">參數</span><span class="sxs-lookup"><span data-stu-id="cb935-122">PARAMETERS</span></span>

### <span data-ttu-id="cb935-123">-動作</span><span class="sxs-lookup"><span data-stu-id="cb935-123">-Action</span></span>
<span data-ttu-id="cb935-124">[允許] 或 [拒絕] 規則。</span><span class="sxs-lookup"><span data-stu-id="cb935-124">Allow or Deny rule.</span></span>

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

### <span data-ttu-id="cb935-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb935-125">-DefaultProfile</span></span>
<span data-ttu-id="cb935-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cb935-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb935-127">-描述</span><span class="sxs-lookup"><span data-stu-id="cb935-127">-Description</span></span>
<span data-ttu-id="cb935-128">[存取限制] 描述。</span><span class="sxs-lookup"><span data-stu-id="cb935-128">Access Restriction description.</span></span>

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

### <span data-ttu-id="cb935-129">-HttpHeader</span><span class="sxs-lookup"><span data-stu-id="cb935-129">-HttpHeader</span></span>
<span data-ttu-id="cb935-130">Http 標頭限制。</span><span class="sxs-lookup"><span data-stu-id="cb935-130">Http header restrictions.</span></span> <span data-ttu-id="cb935-131">範例：-HttpHeader @ {"x-azure-fdid" = "7acacb02-47ea-4cd4-b568-5e880e72582e";' x-轉寄-主機 ' = ' www.contoso.com "，" app.contoso.com "}</span><span class="sxs-lookup"><span data-stu-id="cb935-131">Example: -HttpHeader @{'x-azure-fdid' = '7acacb02-47ea-4cd4-b568-5e880e72582e'; 'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'}</span></span>

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

### <span data-ttu-id="cb935-132">-IgnoreMissingServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="cb935-132">-IgnoreMissingServiceEndpoint</span></span>
<span data-ttu-id="cb935-133">指定是否應驗證子網上的服務端點註冊。</span><span class="sxs-lookup"><span data-stu-id="cb935-133">Specify if Service Endpoint registration at Subnet should be validated.</span></span>

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

### <span data-ttu-id="cb935-134">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="cb935-134">-IpAddress</span></span>
<span data-ttu-id="cb935-135">Ip 位址 v4 或 v6 CIDR 範圍。</span><span class="sxs-lookup"><span data-stu-id="cb935-135">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="cb935-136">例如： 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="cb935-136">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="cb935-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="cb935-137">-Name</span></span>
<span data-ttu-id="cb935-138">規則名稱</span><span class="sxs-lookup"><span data-stu-id="cb935-138">Rule Name</span></span>

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

### <span data-ttu-id="cb935-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb935-139">-PassThru</span></span>
<span data-ttu-id="cb935-140">傳回 [存取限制] 設定物件。</span><span class="sxs-lookup"><span data-stu-id="cb935-140">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="cb935-141">-優先順序</span><span class="sxs-lookup"><span data-stu-id="cb935-141">-Priority</span></span>
<span data-ttu-id="cb935-142">存取限制優先順序。</span><span class="sxs-lookup"><span data-stu-id="cb935-142">Access Restriction priority.</span></span> <span data-ttu-id="cb935-143">例如：500。</span><span class="sxs-lookup"><span data-stu-id="cb935-143">E.g.: 500.</span></span>

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

### <span data-ttu-id="cb935-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb935-144">-ResourceGroupName</span></span>
<span data-ttu-id="cb935-145">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="cb935-145">Resource Group Name</span></span>

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

### <span data-ttu-id="cb935-146">-ServiceTag</span><span class="sxs-lookup"><span data-stu-id="cb935-146">-ServiceTag</span></span>
<span data-ttu-id="cb935-147">服務標記的名稱</span><span class="sxs-lookup"><span data-stu-id="cb935-147">Name of Service Tag</span></span>

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

### <span data-ttu-id="cb935-148">-SlotName</span><span class="sxs-lookup"><span data-stu-id="cb935-148">-SlotName</span></span>
<span data-ttu-id="cb935-149">部署槽名稱。</span><span class="sxs-lookup"><span data-stu-id="cb935-149">Deployment Slot name.</span></span>

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

### <span data-ttu-id="cb935-150">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="cb935-150">-SubnetId</span></span>
<span data-ttu-id="cb935-151">子網上的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="cb935-151">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="cb935-152">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="cb935-152">-SubnetName</span></span>
<span data-ttu-id="cb935-153">子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb935-153">Name of Subnet.</span></span>

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

### <span data-ttu-id="cb935-154">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="cb935-154">-TargetScmSite</span></span>
<span data-ttu-id="cb935-155">規則主要針對主網站或 Scm 網站。</span><span class="sxs-lookup"><span data-stu-id="cb935-155">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="cb935-156">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="cb935-156">-VirtualNetworkName</span></span>
<span data-ttu-id="cb935-157">虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb935-157">Name of Virtual Network.</span></span>

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

### <span data-ttu-id="cb935-158">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="cb935-158">-WebAppName</span></span>
<span data-ttu-id="cb935-159">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb935-159">The name of the web app.</span></span>

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

### <span data-ttu-id="cb935-160">-確認</span><span class="sxs-lookup"><span data-stu-id="cb935-160">-Confirm</span></span>
<span data-ttu-id="cb935-161">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cb935-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb935-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb935-162">-WhatIf</span></span>
<span data-ttu-id="cb935-163">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cb935-163">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb935-164">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb935-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb935-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb935-165">CommonParameters</span></span>
<span data-ttu-id="cb935-166">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb935-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb935-167">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cb935-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb935-168">輸入</span><span class="sxs-lookup"><span data-stu-id="cb935-168">INPUTS</span></span>

### <span data-ttu-id="cb935-169">System.object</span><span class="sxs-lookup"><span data-stu-id="cb935-169">System.String</span></span>

## <span data-ttu-id="cb935-170">輸出</span><span class="sxs-lookup"><span data-stu-id="cb935-170">OUTPUTS</span></span>

### <span data-ttu-id="cb935-171">PSAccessRestrictionConfig 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="cb935-171">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="cb935-172">筆記</span><span class="sxs-lookup"><span data-stu-id="cb935-172">NOTES</span></span>

## <span data-ttu-id="cb935-173">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb935-173">RELATED LINKS</span></span>

[<span data-ttu-id="cb935-174">更新-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="cb935-174">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="cb935-175">AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="cb935-175">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="cb935-176">移除-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="cb935-176">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)

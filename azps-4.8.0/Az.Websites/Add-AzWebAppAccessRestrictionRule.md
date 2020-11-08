---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: 0abad2b3d38a5f614222a8eda7e3c27b9fda9556
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128397"
---
# <span data-ttu-id="53700-101">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="53700-101">Add-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="53700-102">摘要</span><span class="sxs-lookup"><span data-stu-id="53700-102">SYNOPSIS</span></span>
<span data-ttu-id="53700-103">新增 Access Restiction 規則至 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="53700-103">Adds an Access Restiction rule to an Azure Web App.</span></span>

## <span data-ttu-id="53700-104">句法</span><span class="sxs-lookup"><span data-stu-id="53700-104">SYNTAX</span></span>

### <span data-ttu-id="53700-105">IpAddressParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="53700-105">IpAddressParameterSet (Default)</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -IpAddress <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="53700-106">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="53700-106">SubnetNameParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetName <String> -VirtualNetworkName <String> [-IgnoreMissingServiceEndpoint] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53700-107">SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="53700-107">SubnetIdParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetId <String> [-IgnoreMissingServiceEndpoint] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53700-108">說明</span><span class="sxs-lookup"><span data-stu-id="53700-108">DESCRIPTION</span></span>
<span data-ttu-id="53700-109">**AzWebAppAccessRestrictionRule** Cmdlet 會將存取限制規則新增至 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="53700-109">The **Add-AzWebAppAccessRestrictionRule** cmdlet adds an Access Restriction rule to an Azure Web App.</span></span>

## <span data-ttu-id="53700-110">示例</span><span class="sxs-lookup"><span data-stu-id="53700-110">EXAMPLES</span></span>

### <span data-ttu-id="53700-111">範例1：將 IpAddress 存取限制規則新增至 Web App</span><span class="sxs-lookup"><span data-stu-id="53700-111">Example 1: Add IpAddress Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name IpRule -Priority 200 -Action Allow -IpAddress 10.10.0.0/8
```

<span data-ttu-id="53700-112">這個命令會將具有優先順序200和 ip 範圍的訪問限制規則新增到一個名為「ContosoSite」的 Web 應用程式，而該 App 屬於資源群組的 [預設-WestUS]。</span><span class="sxs-lookup"><span data-stu-id="53700-112">This command adds an access restriction rule with priority 200 and ip range to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="53700-113">範例2：新增子網服務端點存取限制規則至 Web App</span><span class="sxs-lookup"><span data-stu-id="53700-113">Example 2: Add Subnet Service Endpoint Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name SubnetRule -Priority 300 -Action Allow -SubnetName appgw-subnet -VirtualNetworkName corp-vnet
```

<span data-ttu-id="53700-114">這個命令會將優先順序為300的 access 限制規則，以及在 corp-vnet 中，將子網 appgw 子網與屬於資源群組 Default-WestUS 的 Web App。</span><span class="sxs-lookup"><span data-stu-id="53700-114">This command adds an access restriction rule with priority 300 and with subnet appgw-subnet in corp-vnet to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="53700-115">參數</span><span class="sxs-lookup"><span data-stu-id="53700-115">PARAMETERS</span></span>

### <span data-ttu-id="53700-116">-動作</span><span class="sxs-lookup"><span data-stu-id="53700-116">-Action</span></span>
<span data-ttu-id="53700-117">[允許] 或 [拒絕] 規則。</span><span class="sxs-lookup"><span data-stu-id="53700-117">Allow or Deny rule.</span></span>

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

### <span data-ttu-id="53700-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53700-118">-DefaultProfile</span></span>
<span data-ttu-id="53700-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="53700-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53700-120">-描述</span><span class="sxs-lookup"><span data-stu-id="53700-120">-Description</span></span>
<span data-ttu-id="53700-121">[存取限制] 描述。</span><span class="sxs-lookup"><span data-stu-id="53700-121">Access Restriction description.</span></span>

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

### <span data-ttu-id="53700-122">-IgnoreMissingServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="53700-122">-IgnoreMissingServiceEndpoint</span></span>
<span data-ttu-id="53700-123">指定是否應驗證子網上的服務端點註冊。</span><span class="sxs-lookup"><span data-stu-id="53700-123">Specify if Service Endpoint registration at Subnet should be validated.</span></span>

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

### <span data-ttu-id="53700-124">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="53700-124">-IpAddress</span></span>
<span data-ttu-id="53700-125">Ip 位址 v4 或 v6 CIDR 範圍。</span><span class="sxs-lookup"><span data-stu-id="53700-125">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="53700-126">例如： 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="53700-126">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="53700-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="53700-127">-Name</span></span>
<span data-ttu-id="53700-128">規則名稱</span><span class="sxs-lookup"><span data-stu-id="53700-128">Rule Name</span></span>

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

### <span data-ttu-id="53700-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53700-129">-PassThru</span></span>
<span data-ttu-id="53700-130">傳回 [存取限制] 設定物件。</span><span class="sxs-lookup"><span data-stu-id="53700-130">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="53700-131">-優先順序</span><span class="sxs-lookup"><span data-stu-id="53700-131">-Priority</span></span>
<span data-ttu-id="53700-132">存取限制優先順序。</span><span class="sxs-lookup"><span data-stu-id="53700-132">Access Restriction priority.</span></span> <span data-ttu-id="53700-133">例如：500。</span><span class="sxs-lookup"><span data-stu-id="53700-133">E.g.: 500.</span></span>

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

### <span data-ttu-id="53700-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53700-134">-ResourceGroupName</span></span>
<span data-ttu-id="53700-135">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="53700-135">Resource Group Name</span></span>

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

### <span data-ttu-id="53700-136">-SlotName</span><span class="sxs-lookup"><span data-stu-id="53700-136">-SlotName</span></span>
<span data-ttu-id="53700-137">部署槽名稱。</span><span class="sxs-lookup"><span data-stu-id="53700-137">Deployment Slot name.</span></span>

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

### <span data-ttu-id="53700-138">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="53700-138">-SubnetId</span></span>
<span data-ttu-id="53700-139">子網上的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="53700-139">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="53700-140">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="53700-140">-SubnetName</span></span>
<span data-ttu-id="53700-141">子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="53700-141">Name of Subnet.</span></span>

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

### <span data-ttu-id="53700-142">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="53700-142">-TargetScmSite</span></span>
<span data-ttu-id="53700-143">規則主要針對主網站或 Scm 網站。</span><span class="sxs-lookup"><span data-stu-id="53700-143">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="53700-144">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="53700-144">-VirtualNetworkName</span></span>
<span data-ttu-id="53700-145">虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="53700-145">Name of Virtual Network.</span></span>

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

### <span data-ttu-id="53700-146">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="53700-146">-WebAppName</span></span>
<span data-ttu-id="53700-147">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="53700-147">The name of the web app.</span></span>

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

### <span data-ttu-id="53700-148">-確認</span><span class="sxs-lookup"><span data-stu-id="53700-148">-Confirm</span></span>
<span data-ttu-id="53700-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="53700-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53700-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53700-150">-WhatIf</span></span>
<span data-ttu-id="53700-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="53700-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="53700-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="53700-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53700-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53700-153">CommonParameters</span></span>
<span data-ttu-id="53700-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="53700-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53700-155">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="53700-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53700-156">輸入</span><span class="sxs-lookup"><span data-stu-id="53700-156">INPUTS</span></span>

### <span data-ttu-id="53700-157">System.object</span><span class="sxs-lookup"><span data-stu-id="53700-157">System.String</span></span>

## <span data-ttu-id="53700-158">輸出</span><span class="sxs-lookup"><span data-stu-id="53700-158">OUTPUTS</span></span>

### <span data-ttu-id="53700-159">PSAccessRestrictionConfig 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="53700-159">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="53700-160">筆記</span><span class="sxs-lookup"><span data-stu-id="53700-160">NOTES</span></span>

## <span data-ttu-id="53700-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="53700-161">RELATED LINKS</span></span>

[<span data-ttu-id="53700-162">更新-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="53700-162">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="53700-163">AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="53700-163">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="53700-164">移除-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="53700-164">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
ms.openlocfilehash: e5cef84d4ae45e4ce55b1f377ab16edc2449c72c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904434"
---
# <span data-ttu-id="567c7-101">Get-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="567c7-101">Get-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="567c7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="567c7-102">SYNOPSIS</span></span>
<span data-ttu-id="567c7-103">取得應用程式群組。</span><span class="sxs-lookup"><span data-stu-id="567c7-103">Get an application group.</span></span>

## <span data-ttu-id="567c7-104">語法</span><span class="sxs-lookup"><span data-stu-id="567c7-104">SYNTAX</span></span>

### <span data-ttu-id="567c7-105">清單1 (預設) </span><span class="sxs-lookup"><span data-stu-id="567c7-105">List1 (Default)</span></span>
```
Get-AzWvdApplicationGroup [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="567c7-106">獲取</span><span class="sxs-lookup"><span data-stu-id="567c7-106">Get</span></span>
```
Get-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="567c7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="567c7-107">GetViaIdentity</span></span>
```
Get-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="567c7-108">清單</span><span class="sxs-lookup"><span data-stu-id="567c7-108">List</span></span>
```
Get-AzWvdApplicationGroup -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="567c7-109">描述</span><span class="sxs-lookup"><span data-stu-id="567c7-109">DESCRIPTION</span></span>
<span data-ttu-id="567c7-110">取得應用程式群組。</span><span class="sxs-lookup"><span data-stu-id="567c7-110">Get an application group.</span></span>

## <span data-ttu-id="567c7-111">例子</span><span class="sxs-lookup"><span data-stu-id="567c7-111">EXAMPLES</span></span>

### <span data-ttu-id="567c7-112">範例 1：根據名稱取得 Windows 虛擬桌面應用程式組</span><span class="sxs-lookup"><span data-stu-id="567c7-112">Example 1: Get a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="567c7-113">此命令會獲得資源群組中的 Windows 虛擬桌面應用程式群組。</span><span class="sxs-lookup"><span data-stu-id="567c7-113">This command gets a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="567c7-114">範例 2：列出 Windows 虛擬桌面應用程式工作組</span><span class="sxs-lookup"><span data-stu-id="567c7-114">Example 2: List Windows Virtual Desktop ApplicationGroups</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName

Location   Name                  Type
--------   ----                  ----
eastus     ApplicationGroupName1 Microsoft.DesktopVirtualization/applicationgroups
eastus     ApplicationGroupName2 Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="567c7-115">此命令會列出資源群組中的 Windows 虛擬桌面應用程式群組。</span><span class="sxs-lookup"><span data-stu-id="567c7-115">This command lists a Windows Virtual Desktop ApplicationGroups in a Resource Group.</span></span>

## <span data-ttu-id="567c7-116">參數</span><span class="sxs-lookup"><span data-stu-id="567c7-116">PARAMETERS</span></span>

### <span data-ttu-id="567c7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="567c7-117">-DefaultProfile</span></span>
<span data-ttu-id="567c7-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="567c7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="567c7-119">-篩選</span><span class="sxs-lookup"><span data-stu-id="567c7-119">-Filter</span></span>
<span data-ttu-id="567c7-120">OData 篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="567c7-120">OData filter expression.</span></span>
<span data-ttu-id="567c7-121">篩選的有效屬性為 applicationGroupType。</span><span class="sxs-lookup"><span data-stu-id="567c7-121">Valid properties for filtering are applicationGroupType.</span></span>

```yaml
Type: System.String
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="567c7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="567c7-122">-InputObject</span></span>
<span data-ttu-id="567c7-123">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="567c7-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="567c7-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="567c7-124">-Name</span></span>
<span data-ttu-id="567c7-125">應用程式組的名稱</span><span class="sxs-lookup"><span data-stu-id="567c7-125">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="567c7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="567c7-126">-ResourceGroupName</span></span>
<span data-ttu-id="567c7-127">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="567c7-127">The name of the resource group.</span></span>
<span data-ttu-id="567c7-128">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="567c7-128">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="567c7-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="567c7-129">-SubscriptionId</span></span>
<span data-ttu-id="567c7-130">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="567c7-130">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="567c7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="567c7-131">CommonParameters</span></span>
<span data-ttu-id="567c7-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="567c7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="567c7-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="567c7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="567c7-134">輸入</span><span class="sxs-lookup"><span data-stu-id="567c7-134">INPUTS</span></span>

### <span data-ttu-id="567c7-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="567c7-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="567c7-136">輸出</span><span class="sxs-lookup"><span data-stu-id="567c7-136">OUTPUTS</span></span>

### <span data-ttu-id="567c7-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="567c7-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="567c7-138">筆記</span><span class="sxs-lookup"><span data-stu-id="567c7-138">NOTES</span></span>

<span data-ttu-id="567c7-139">別名</span><span class="sxs-lookup"><span data-stu-id="567c7-139">ALIASES</span></span>

<span data-ttu-id="567c7-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="567c7-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="567c7-141">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="567c7-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="567c7-142">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="567c7-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="567c7-143">INPUTOBJECT： <IDesktopVirtualizationIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="567c7-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="567c7-144">`[ApplicationGroupName <String>]`：應用程式組的名稱</span><span class="sxs-lookup"><span data-stu-id="567c7-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="567c7-145">`[ApplicationName <String>]`：指定應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="567c7-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="567c7-146">`[DesktopName <String>]`：指定桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="567c7-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="567c7-147">`[HostPoolName <String>]`：指定資源群組內的主機組名</span><span class="sxs-lookup"><span data-stu-id="567c7-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="567c7-148">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="567c7-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="567c7-149">`[MsixPackageFullName <String>]`：指定主機多工緩衝處理程式中 MSIX 套件的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="567c7-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="567c7-150">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="567c7-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="567c7-151">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="567c7-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="567c7-152">`[SessionHostName <String>]`：指定主機集中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="567c7-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="567c7-153">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="567c7-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="567c7-154">`[UserSessionId <String>]`：指定工作階段主機內的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="567c7-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="567c7-155">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="567c7-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="567c7-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="567c7-156">RELATED LINKS</span></span>


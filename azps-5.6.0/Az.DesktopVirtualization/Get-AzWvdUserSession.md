---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
ms.openlocfilehash: a19d1e39fb9ef2e982b569b8c0351d8d1bde1fb2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905466"
---
# <span data-ttu-id="5dcdc-101">Get-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="5dcdc-101">Get-AzWvdUserSession</span></span>

## <span data-ttu-id="5dcdc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5dcdc-102">SYNOPSIS</span></span>
<span data-ttu-id="5dcdc-103">取得使用者Session。</span><span class="sxs-lookup"><span data-stu-id="5dcdc-103">Get a userSession.</span></span>

## <span data-ttu-id="5dcdc-104">語法</span><span class="sxs-lookup"><span data-stu-id="5dcdc-104">SYNTAX</span></span>

### <span data-ttu-id="5dcdc-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="5dcdc-105">List (Default)</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5dcdc-106">獲取</span><span class="sxs-lookup"><span data-stu-id="5dcdc-106">Get</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5dcdc-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5dcdc-107">GetViaIdentity</span></span>
```
Get-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="5dcdc-108">清單1</span><span class="sxs-lookup"><span data-stu-id="5dcdc-108">List1</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5dcdc-109">描述</span><span class="sxs-lookup"><span data-stu-id="5dcdc-109">DESCRIPTION</span></span>
<span data-ttu-id="5dcdc-110">取得使用者Session。</span><span class="sxs-lookup"><span data-stu-id="5dcdc-110">Get a userSession.</span></span>

## <span data-ttu-id="5dcdc-111">例子</span><span class="sxs-lookup"><span data-stu-id="5dcdc-111">EXAMPLES</span></span>

### <span data-ttu-id="5dcdc-112">範例 1：取得 Windows 虛擬桌面使用者名稱</span><span class="sxs-lookup"><span data-stu-id="5dcdc-112">Example 1: Get a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="5dcdc-113">此命令在工作階段主機中會獲得 Windows 虛擬桌面使用者部署。</span><span class="sxs-lookup"><span data-stu-id="5dcdc-113">This command gets a Windows Virtual Desktop UserSession in a Session Host.</span></span>

### <span data-ttu-id="5dcdc-114">範例 2：列出 Windows 虛擬桌面使用者</span><span class="sxs-lookup"><span data-stu-id="5dcdc-114">Example 2: List Windows Virtual Desktop UserSessions</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="5dcdc-115">此命令會列出工作階段主機中的 Windows 虛擬桌面使用者清單。</span><span class="sxs-lookup"><span data-stu-id="5dcdc-115">This command lists a Windows Virtual Desktop UserSessions in a Session Host.</span></span>

### <span data-ttu-id="5dcdc-116">範例 3：在主機集中列出 Windows 虛擬桌面使用者</span><span class="sxs-lookup"><span data-stu-id="5dcdc-116">Example 3: List Windows Virtual Desktop UserSessions in host pool</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="5dcdc-117">此命令會列出主機集中工作階段主機中的 Windows 虛擬桌面使用者清單。</span><span class="sxs-lookup"><span data-stu-id="5dcdc-117">This command lists a Windows Virtual Desktop UserSessions in a Session Host in a host pool.</span></span>

## <span data-ttu-id="5dcdc-118">參數</span><span class="sxs-lookup"><span data-stu-id="5dcdc-118">PARAMETERS</span></span>

### <span data-ttu-id="5dcdc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dcdc-119">-DefaultProfile</span></span>
<span data-ttu-id="5dcdc-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5dcdc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5dcdc-121">-篩選</span><span class="sxs-lookup"><span data-stu-id="5dcdc-121">-Filter</span></span>
<span data-ttu-id="5dcdc-122">OData 篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="5dcdc-122">OData filter expression.</span></span>
<span data-ttu-id="5dcdc-123">篩選的有效屬性為 userprincipalname 和會話狀態。</span><span class="sxs-lookup"><span data-stu-id="5dcdc-123">Valid properties for filtering are userprincipalname and sessionstate.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dcdc-124">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="5dcdc-124">-HostPoolName</span></span>
<span data-ttu-id="5dcdc-125">指定資源群組內的主機組名</span><span class="sxs-lookup"><span data-stu-id="5dcdc-125">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dcdc-126">-Id</span><span class="sxs-lookup"><span data-stu-id="5dcdc-126">-Id</span></span>
<span data-ttu-id="5dcdc-127">指定工作階段主機內的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="5dcdc-127">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dcdc-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5dcdc-128">-InputObject</span></span>
<span data-ttu-id="5dcdc-129">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5dcdc-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5dcdc-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dcdc-130">-ResourceGroupName</span></span>
<span data-ttu-id="5dcdc-131">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5dcdc-131">The name of the resource group.</span></span>
<span data-ttu-id="5dcdc-132">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="5dcdc-132">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dcdc-133">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="5dcdc-133">-SessionHostName</span></span>
<span data-ttu-id="5dcdc-134">指定主機集中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="5dcdc-134">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dcdc-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5dcdc-135">-SubscriptionId</span></span>
<span data-ttu-id="5dcdc-136">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5dcdc-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5dcdc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dcdc-137">CommonParameters</span></span>
<span data-ttu-id="5dcdc-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5dcdc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dcdc-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5dcdc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dcdc-140">輸入</span><span class="sxs-lookup"><span data-stu-id="5dcdc-140">INPUTS</span></span>

### <span data-ttu-id="5dcdc-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="5dcdc-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="5dcdc-142">輸出</span><span class="sxs-lookup"><span data-stu-id="5dcdc-142">OUTPUTS</span></span>

### <span data-ttu-id="5dcdc-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.Api20201102Preview.IUserSession</span><span class="sxs-lookup"><span data-stu-id="5dcdc-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IUserSession</span></span>

## <span data-ttu-id="5dcdc-144">筆記</span><span class="sxs-lookup"><span data-stu-id="5dcdc-144">NOTES</span></span>

<span data-ttu-id="5dcdc-145">別名</span><span class="sxs-lookup"><span data-stu-id="5dcdc-145">ALIASES</span></span>

<span data-ttu-id="5dcdc-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="5dcdc-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5dcdc-147">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5dcdc-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5dcdc-148">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="5dcdc-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5dcdc-149">INPUTOBJECT： <IDesktopVirtualizationIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="5dcdc-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5dcdc-150">`[ApplicationGroupName <String>]`：應用程式組的名稱</span><span class="sxs-lookup"><span data-stu-id="5dcdc-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="5dcdc-151">`[ApplicationName <String>]`：指定應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="5dcdc-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="5dcdc-152">`[DesktopName <String>]`：指定桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="5dcdc-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="5dcdc-153">`[HostPoolName <String>]`：指定資源群組內的主機組名</span><span class="sxs-lookup"><span data-stu-id="5dcdc-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="5dcdc-154">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="5dcdc-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5dcdc-155">`[MsixPackageFullName <String>]`：指定主機多工緩衝處理程式中 MSIX 套件的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="5dcdc-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="5dcdc-156">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5dcdc-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5dcdc-157">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="5dcdc-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="5dcdc-158">`[SessionHostName <String>]`：指定主機集中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="5dcdc-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="5dcdc-159">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5dcdc-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5dcdc-160">`[UserSessionId <String>]`：指定工作階段主機內的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="5dcdc-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="5dcdc-161">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="5dcdc-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="5dcdc-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="5dcdc-162">RELATED LINKS</span></span>


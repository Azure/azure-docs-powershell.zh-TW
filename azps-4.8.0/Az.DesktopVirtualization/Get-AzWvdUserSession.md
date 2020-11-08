---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
ms.openlocfilehash: eedf639ebf5c25ff9153072a337ea659b41a9e92
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128203"
---
# <span data-ttu-id="94ce5-101">Get-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="94ce5-101">Get-AzWvdUserSession</span></span>

## <span data-ttu-id="94ce5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="94ce5-102">SYNOPSIS</span></span>
<span data-ttu-id="94ce5-103">取得 userSession。</span><span class="sxs-lookup"><span data-stu-id="94ce5-103">Get a userSession.</span></span>

## <span data-ttu-id="94ce5-104">句法</span><span class="sxs-lookup"><span data-stu-id="94ce5-104">SYNTAX</span></span>

### <span data-ttu-id="94ce5-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="94ce5-105">List (Default)</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="94ce5-106">獲取</span><span class="sxs-lookup"><span data-stu-id="94ce5-106">Get</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="94ce5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="94ce5-107">GetViaIdentity</span></span>
```
Get-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="94ce5-108">List1</span><span class="sxs-lookup"><span data-stu-id="94ce5-108">List1</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="94ce5-109">說明</span><span class="sxs-lookup"><span data-stu-id="94ce5-109">DESCRIPTION</span></span>
<span data-ttu-id="94ce5-110">取得 userSession。</span><span class="sxs-lookup"><span data-stu-id="94ce5-110">Get a userSession.</span></span>

## <span data-ttu-id="94ce5-111">示例</span><span class="sxs-lookup"><span data-stu-id="94ce5-111">EXAMPLES</span></span>

### <span data-ttu-id="94ce5-112">範例1：依名稱取得 Windows 虛擬桌面 UserSession</span><span class="sxs-lookup"><span data-stu-id="94ce5-112">Example 1: Get a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="94ce5-113">這個命令會在工作階段主機中取得 Windows 虛擬桌面 UserSession。</span><span class="sxs-lookup"><span data-stu-id="94ce5-113">This command gets a Windows Virtual Desktop UserSession in a Session Host.</span></span>

### <span data-ttu-id="94ce5-114">範例2：列出 Windows 虛擬桌面 UserSessions</span><span class="sxs-lookup"><span data-stu-id="94ce5-114">Example 2: List Windows Virtual Desktop UserSessions</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="94ce5-115">這個命令會在工作階段主機中列出 Windows 虛擬桌面 UserSessions。</span><span class="sxs-lookup"><span data-stu-id="94ce5-115">This command lists a Windows Virtual Desktop UserSessions in a Session Host.</span></span>

### <span data-ttu-id="94ce5-116">範例3：在主機池中列出 Windows 虛擬桌面 UserSessions</span><span class="sxs-lookup"><span data-stu-id="94ce5-116">Example 3: List Windows Virtual Desktop UserSessions in host pool</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="94ce5-117">這個命令會列出主機池中的工作階段主機中的 Windows 虛擬桌面 UserSessions。</span><span class="sxs-lookup"><span data-stu-id="94ce5-117">This command lists a Windows Virtual Desktop UserSessions in a Session Host in a host pool.</span></span>

## <span data-ttu-id="94ce5-118">參數</span><span class="sxs-lookup"><span data-stu-id="94ce5-118">PARAMETERS</span></span>

### <span data-ttu-id="94ce5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94ce5-119">-DefaultProfile</span></span>
<span data-ttu-id="94ce5-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="94ce5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94ce5-121">-篩選</span><span class="sxs-lookup"><span data-stu-id="94ce5-121">-Filter</span></span>
<span data-ttu-id="94ce5-122">OData 篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="94ce5-122">OData filter expression.</span></span>
<span data-ttu-id="94ce5-123">篩選的有效屬性為 userprincipalname 與 sessionstate。</span><span class="sxs-lookup"><span data-stu-id="94ce5-123">Valid properties for filtering are userprincipalname and sessionstate.</span></span>

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

### <span data-ttu-id="94ce5-124">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="94ce5-124">-HostPoolName</span></span>
<span data-ttu-id="94ce5-125">指定資源群組中主機池的名稱</span><span class="sxs-lookup"><span data-stu-id="94ce5-125">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="94ce5-126">-識別碼</span><span class="sxs-lookup"><span data-stu-id="94ce5-126">-Id</span></span>
<span data-ttu-id="94ce5-127">指定的工作階段主機中使用者會話的名稱</span><span class="sxs-lookup"><span data-stu-id="94ce5-127">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="94ce5-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94ce5-128">-InputObject</span></span>
<span data-ttu-id="94ce5-129">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="94ce5-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="94ce5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94ce5-130">-ResourceGroupName</span></span>
<span data-ttu-id="94ce5-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="94ce5-131">The name of the resource group.</span></span>
<span data-ttu-id="94ce5-132">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="94ce5-132">The name is case insensitive.</span></span>

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

### <span data-ttu-id="94ce5-133">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="94ce5-133">-SessionHostName</span></span>
<span data-ttu-id="94ce5-134">指定主機池中工作階段主機的名稱</span><span class="sxs-lookup"><span data-stu-id="94ce5-134">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="94ce5-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="94ce5-135">-SubscriptionId</span></span>
<span data-ttu-id="94ce5-136">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="94ce5-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="94ce5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94ce5-137">CommonParameters</span></span>
<span data-ttu-id="94ce5-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="94ce5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94ce5-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="94ce5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94ce5-140">輸入</span><span class="sxs-lookup"><span data-stu-id="94ce5-140">INPUTS</span></span>

### <span data-ttu-id="94ce5-141">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="94ce5-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="94ce5-142">輸出</span><span class="sxs-lookup"><span data-stu-id="94ce5-142">OUTPUTS</span></span>

### <span data-ttu-id="94ce5-143">IUserSession （DesktopVirtualization）。 Api20191210Preview。</span><span class="sxs-lookup"><span data-stu-id="94ce5-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IUserSession</span></span>

## <span data-ttu-id="94ce5-144">筆記</span><span class="sxs-lookup"><span data-stu-id="94ce5-144">NOTES</span></span>

<span data-ttu-id="94ce5-145">別名</span><span class="sxs-lookup"><span data-stu-id="94ce5-145">ALIASES</span></span>

<span data-ttu-id="94ce5-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="94ce5-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="94ce5-147">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="94ce5-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="94ce5-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="94ce5-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="94ce5-149">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="94ce5-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="94ce5-150">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="94ce5-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="94ce5-151">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="94ce5-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="94ce5-152">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="94ce5-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="94ce5-153">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="94ce5-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="94ce5-154">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="94ce5-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="94ce5-155">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="94ce5-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="94ce5-156">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="94ce5-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="94ce5-157">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="94ce5-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="94ce5-158">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="94ce5-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="94ce5-159">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="94ce5-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="94ce5-160">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="94ce5-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="94ce5-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="94ce5-161">RELATED LINKS</span></span>


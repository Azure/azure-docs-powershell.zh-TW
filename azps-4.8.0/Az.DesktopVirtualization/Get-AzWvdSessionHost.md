---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
ms.openlocfilehash: 94f4c5ad9c401c429c9ef2f2f1c146f83a407196
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971116"
---
# <span data-ttu-id="f4888-101">Get-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="f4888-101">Get-AzWvdSessionHost</span></span>

## <span data-ttu-id="f4888-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f4888-102">SYNOPSIS</span></span>
<span data-ttu-id="f4888-103">取得工作階段主機。</span><span class="sxs-lookup"><span data-stu-id="f4888-103">Get a session host.</span></span>

## <span data-ttu-id="f4888-104">句法</span><span class="sxs-lookup"><span data-stu-id="f4888-104">SYNTAX</span></span>

### <span data-ttu-id="f4888-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="f4888-105">List (Default)</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f4888-106">獲取</span><span class="sxs-lookup"><span data-stu-id="f4888-106">Get</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f4888-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f4888-107">GetViaIdentity</span></span>
```
Get-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4888-108">說明</span><span class="sxs-lookup"><span data-stu-id="f4888-108">DESCRIPTION</span></span>
<span data-ttu-id="f4888-109">取得工作階段主機。</span><span class="sxs-lookup"><span data-stu-id="f4888-109">Get a session host.</span></span>

## <span data-ttu-id="f4888-110">示例</span><span class="sxs-lookup"><span data-stu-id="f4888-110">EXAMPLES</span></span>

### <span data-ttu-id="f4888-111">範例1：依名稱取得 Windows 虛擬桌面 SessionHost</span><span class="sxs-lookup"><span data-stu-id="f4888-111">Example 1: Get a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="f4888-112">這個命令會在主機池中取得 Windows 虛擬桌面 SessionHost。</span><span class="sxs-lookup"><span data-stu-id="f4888-112">This command gets a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

### <span data-ttu-id="f4888-113">範例2：列出 Windows 虛擬桌面 SessionHosts</span><span class="sxs-lookup"><span data-stu-id="f4888-113">Example 2: List Windows Virtual Desktop SessionHosts</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName1 Microsoft.DesktopVirtualization/hostpools/sessionhosts
HostPoolName/SessionHostName2 Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="f4888-114">這個命令會在主機池中列出 Windows 虛擬桌面 SessionHosts。</span><span class="sxs-lookup"><span data-stu-id="f4888-114">This command lists a Windows Virtual Desktop SessionHosts in a Host Pool.</span></span>

## <span data-ttu-id="f4888-115">參數</span><span class="sxs-lookup"><span data-stu-id="f4888-115">PARAMETERS</span></span>

### <span data-ttu-id="f4888-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4888-116">-DefaultProfile</span></span>
<span data-ttu-id="f4888-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4888-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4888-118">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="f4888-118">-HostPoolName</span></span>
<span data-ttu-id="f4888-119">指定資源群組中主機池的名稱</span><span class="sxs-lookup"><span data-stu-id="f4888-119">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="f4888-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4888-120">-InputObject</span></span>
<span data-ttu-id="f4888-121">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f4888-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f4888-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="f4888-122">-Name</span></span>
<span data-ttu-id="f4888-123">指定主機池中工作階段主機的名稱</span><span class="sxs-lookup"><span data-stu-id="f4888-123">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4888-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4888-124">-ResourceGroupName</span></span>
<span data-ttu-id="f4888-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4888-125">The name of the resource group.</span></span>
<span data-ttu-id="f4888-126">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="f4888-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f4888-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f4888-127">-SubscriptionId</span></span>
<span data-ttu-id="f4888-128">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="f4888-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4888-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4888-129">CommonParameters</span></span>
<span data-ttu-id="f4888-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f4888-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4888-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f4888-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4888-132">輸入</span><span class="sxs-lookup"><span data-stu-id="f4888-132">INPUTS</span></span>

### <span data-ttu-id="f4888-133">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="f4888-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="f4888-134">輸出</span><span class="sxs-lookup"><span data-stu-id="f4888-134">OUTPUTS</span></span>

### <span data-ttu-id="f4888-135">ISessionHost （DesktopVirtualization）。 Api20191210Preview。</span><span class="sxs-lookup"><span data-stu-id="f4888-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.ISessionHost</span></span>

## <span data-ttu-id="f4888-136">筆記</span><span class="sxs-lookup"><span data-stu-id="f4888-136">NOTES</span></span>

<span data-ttu-id="f4888-137">別名</span><span class="sxs-lookup"><span data-stu-id="f4888-137">ALIASES</span></span>

<span data-ttu-id="f4888-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="f4888-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f4888-139">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="f4888-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f4888-140">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="f4888-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f4888-141">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="f4888-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f4888-142">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="f4888-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="f4888-143">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="f4888-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="f4888-144">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="f4888-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="f4888-145">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="f4888-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="f4888-146">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="f4888-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f4888-147">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4888-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f4888-148">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="f4888-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="f4888-149">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="f4888-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="f4888-150">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f4888-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f4888-151">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="f4888-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="f4888-152">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="f4888-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="f4888-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4888-153">RELATED LINKS</span></span>


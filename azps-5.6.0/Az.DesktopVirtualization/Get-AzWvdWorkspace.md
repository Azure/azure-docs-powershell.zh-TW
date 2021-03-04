---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdWorkspace.md
ms.openlocfilehash: 331026116b59e71d57b4ea440b53a1445ea7642b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909061"
---
# <span data-ttu-id="ca62c-101">Get-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="ca62c-101">Get-AzWvdWorkspace</span></span>

## <span data-ttu-id="ca62c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ca62c-102">SYNOPSIS</span></span>
<span data-ttu-id="ca62c-103">取得工作區。</span><span class="sxs-lookup"><span data-stu-id="ca62c-103">Get a workspace.</span></span>

## <span data-ttu-id="ca62c-104">語法</span><span class="sxs-lookup"><span data-stu-id="ca62c-104">SYNTAX</span></span>

### <span data-ttu-id="ca62c-105">清單1 (預設) </span><span class="sxs-lookup"><span data-stu-id="ca62c-105">List1 (Default)</span></span>
```
Get-AzWvdWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ca62c-106">獲取</span><span class="sxs-lookup"><span data-stu-id="ca62c-106">Get</span></span>
```
Get-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ca62c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ca62c-107">GetViaIdentity</span></span>
```
Get-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="ca62c-108">清單</span><span class="sxs-lookup"><span data-stu-id="ca62c-108">List</span></span>
```
Get-AzWvdWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca62c-109">描述</span><span class="sxs-lookup"><span data-stu-id="ca62c-109">DESCRIPTION</span></span>
<span data-ttu-id="ca62c-110">取得工作區。</span><span class="sxs-lookup"><span data-stu-id="ca62c-110">Get a workspace.</span></span>

## <span data-ttu-id="ca62c-111">例子</span><span class="sxs-lookup"><span data-stu-id="ca62c-111">EXAMPLES</span></span>

### <span data-ttu-id="ca62c-112">範例 1：按名稱取得 Windows 虛擬桌面工作區</span><span class="sxs-lookup"><span data-stu-id="ca62c-112">Example 1: Get a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> Get-AzWvdWorkspace -ResourceGroupName ResourceGroupName -Name WorkspaceName

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="ca62c-113">此命令在資源群組中會獲得 Windows 虛擬桌面工作區。</span><span class="sxs-lookup"><span data-stu-id="ca62c-113">This command gets a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="ca62c-114">範例 2：列出 Windows 虛擬桌面工作區</span><span class="sxs-lookup"><span data-stu-id="ca62c-114">Example 2: List Windows Virtual Desktop Workspaces</span></span>
```powershell
PS C:\> Get-AzWvdWorkspace -ResourceGroupName ResourceGroupName

Location   Name           Type
--------   ----           ----
eastus     WorkspaceName1 Microsoft.DesktopVirtualization/workspaces
eastus     WorkspaceName2 Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="ca62c-115">此命令會列出資源群組中的 Windows 虛擬桌面工作區。</span><span class="sxs-lookup"><span data-stu-id="ca62c-115">This command lists a Windows Virtual Desktop Workspaces in a Resource Group.</span></span>

## <span data-ttu-id="ca62c-116">參數</span><span class="sxs-lookup"><span data-stu-id="ca62c-116">PARAMETERS</span></span>

### <span data-ttu-id="ca62c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca62c-117">-DefaultProfile</span></span>
<span data-ttu-id="ca62c-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ca62c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca62c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca62c-119">-InputObject</span></span>
<span data-ttu-id="ca62c-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ca62c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ca62c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="ca62c-121">-Name</span></span>
<span data-ttu-id="ca62c-122">工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="ca62c-122">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca62c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca62c-123">-ResourceGroupName</span></span>
<span data-ttu-id="ca62c-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca62c-124">The name of the resource group.</span></span>
<span data-ttu-id="ca62c-125">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="ca62c-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ca62c-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ca62c-126">-SubscriptionId</span></span>
<span data-ttu-id="ca62c-127">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ca62c-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ca62c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca62c-128">CommonParameters</span></span>
<span data-ttu-id="ca62c-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ca62c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca62c-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca62c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca62c-131">輸入</span><span class="sxs-lookup"><span data-stu-id="ca62c-131">INPUTS</span></span>

### <span data-ttu-id="ca62c-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="ca62c-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="ca62c-133">輸出</span><span class="sxs-lookup"><span data-stu-id="ca62c-133">OUTPUTS</span></span>

### <span data-ttu-id="ca62c-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.Api20201102Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="ca62c-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="ca62c-135">筆記</span><span class="sxs-lookup"><span data-stu-id="ca62c-135">NOTES</span></span>

<span data-ttu-id="ca62c-136">別名</span><span class="sxs-lookup"><span data-stu-id="ca62c-136">ALIASES</span></span>

<span data-ttu-id="ca62c-137">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="ca62c-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ca62c-138">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ca62c-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ca62c-139">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="ca62c-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ca62c-140">INPUTOBJECT： <IDesktopVirtualizationIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="ca62c-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ca62c-141">`[ApplicationGroupName <String>]`：應用程式組的名稱</span><span class="sxs-lookup"><span data-stu-id="ca62c-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="ca62c-142">`[ApplicationName <String>]`：指定應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="ca62c-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="ca62c-143">`[DesktopName <String>]`：指定桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="ca62c-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="ca62c-144">`[HostPoolName <String>]`：指定資源群組內的主機組名</span><span class="sxs-lookup"><span data-stu-id="ca62c-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="ca62c-145">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="ca62c-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ca62c-146">`[MsixPackageFullName <String>]`：指定主機多工緩衝處理程式中 MSIX 套件的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="ca62c-146">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="ca62c-147">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca62c-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ca62c-148">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="ca62c-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="ca62c-149">`[SessionHostName <String>]`：指定主機集中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="ca62c-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="ca62c-150">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ca62c-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ca62c-151">`[UserSessionId <String>]`：指定工作階段主機內的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="ca62c-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="ca62c-152">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="ca62c-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="ca62c-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca62c-153">RELATED LINKS</span></span>


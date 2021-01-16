---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdWorkspace.md
ms.openlocfilehash: b17fedefcac1acd260f9b3f0cf8834605a590ca9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284143"
---
# <span data-ttu-id="93c37-101">Get-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="93c37-101">Get-AzWvdWorkspace</span></span>

## <span data-ttu-id="93c37-102">摘要</span><span class="sxs-lookup"><span data-stu-id="93c37-102">SYNOPSIS</span></span>
<span data-ttu-id="93c37-103">取得工作區。</span><span class="sxs-lookup"><span data-stu-id="93c37-103">Get a workspace.</span></span>

## <span data-ttu-id="93c37-104">句法</span><span class="sxs-lookup"><span data-stu-id="93c37-104">SYNTAX</span></span>

### <span data-ttu-id="93c37-105">List1 (預設) </span><span class="sxs-lookup"><span data-stu-id="93c37-105">List1 (Default)</span></span>
```
Get-AzWvdWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="93c37-106">獲取</span><span class="sxs-lookup"><span data-stu-id="93c37-106">Get</span></span>
```
Get-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="93c37-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="93c37-107">GetViaIdentity</span></span>
```
Get-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="93c37-108">清單</span><span class="sxs-lookup"><span data-stu-id="93c37-108">List</span></span>
```
Get-AzWvdWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="93c37-109">說明</span><span class="sxs-lookup"><span data-stu-id="93c37-109">DESCRIPTION</span></span>
<span data-ttu-id="93c37-110">取得工作區。</span><span class="sxs-lookup"><span data-stu-id="93c37-110">Get a workspace.</span></span>

## <span data-ttu-id="93c37-111">示例</span><span class="sxs-lookup"><span data-stu-id="93c37-111">EXAMPLES</span></span>

### <span data-ttu-id="93c37-112">範例1：依名稱取得 Windows 虛擬桌面工作區</span><span class="sxs-lookup"><span data-stu-id="93c37-112">Example 1: Get a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> Get-AzWvdWorkspace -ResourceGroupName ResourceGroupName -Name WorkspaceName

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="93c37-113">這個命令會在資源群組中取得 Windows 虛擬桌面工作區。</span><span class="sxs-lookup"><span data-stu-id="93c37-113">This command gets a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="93c37-114">範例2：列出 Windows 虛擬桌面工作區</span><span class="sxs-lookup"><span data-stu-id="93c37-114">Example 2: List Windows Virtual Desktop Workspaces</span></span>
```powershell
PS C:\> Get-AzWvdWorkspace -ResourceGroupName ResourceGroupName

Location   Name           Type
--------   ----           ----
eastus     WorkspaceName1 Microsoft.DesktopVirtualization/workspaces
eastus     WorkspaceName2 Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="93c37-115">這個命令會列出資源群組中的 Windows 虛擬桌面工作區。</span><span class="sxs-lookup"><span data-stu-id="93c37-115">This command lists a Windows Virtual Desktop Workspaces in a Resource Group.</span></span>

## <span data-ttu-id="93c37-116">參數</span><span class="sxs-lookup"><span data-stu-id="93c37-116">PARAMETERS</span></span>

### <span data-ttu-id="93c37-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93c37-117">-DefaultProfile</span></span>
<span data-ttu-id="93c37-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="93c37-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93c37-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93c37-119">-InputObject</span></span>
<span data-ttu-id="93c37-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="93c37-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="93c37-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="93c37-121">-Name</span></span>
<span data-ttu-id="93c37-122">工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="93c37-122">The name of the workspace</span></span>

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

### <span data-ttu-id="93c37-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93c37-123">-ResourceGroupName</span></span>
<span data-ttu-id="93c37-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="93c37-124">The name of the resource group.</span></span>
<span data-ttu-id="93c37-125">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="93c37-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="93c37-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93c37-126">-SubscriptionId</span></span>
<span data-ttu-id="93c37-127">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="93c37-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="93c37-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93c37-128">CommonParameters</span></span>
<span data-ttu-id="93c37-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="93c37-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93c37-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="93c37-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93c37-131">輸入</span><span class="sxs-lookup"><span data-stu-id="93c37-131">INPUTS</span></span>

### <span data-ttu-id="93c37-132">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="93c37-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="93c37-133">輸出</span><span class="sxs-lookup"><span data-stu-id="93c37-133">OUTPUTS</span></span>

### <span data-ttu-id="93c37-134">IWorkspace （DesktopVirtualization）。 Api20201019Preview。</span><span class="sxs-lookup"><span data-stu-id="93c37-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IWorkspace</span></span>

## <span data-ttu-id="93c37-135">筆記</span><span class="sxs-lookup"><span data-stu-id="93c37-135">NOTES</span></span>

<span data-ttu-id="93c37-136">別名</span><span class="sxs-lookup"><span data-stu-id="93c37-136">ALIASES</span></span>

<span data-ttu-id="93c37-137">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="93c37-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="93c37-138">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="93c37-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="93c37-139">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="93c37-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="93c37-140">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="93c37-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="93c37-141">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="93c37-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="93c37-142">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="93c37-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="93c37-143">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="93c37-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="93c37-144">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="93c37-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="93c37-145">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="93c37-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="93c37-146">`[MsixPackageFullName <String>]`： MSIX 套件在指定 hostpool 中的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="93c37-146">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="93c37-147">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="93c37-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="93c37-148">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="93c37-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="93c37-149">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="93c37-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="93c37-150">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="93c37-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="93c37-151">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="93c37-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="93c37-152">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="93c37-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="93c37-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="93c37-153">RELATED LINKS</span></span>


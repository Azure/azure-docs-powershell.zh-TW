---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
ms.openlocfilehash: b7aa21b07726140f8f6514fe8d7b6dc9a4b191dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904437"
---
# <span data-ttu-id="3bea3-101">Get-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="3bea3-101">Get-AzWvdApplication</span></span>

## <span data-ttu-id="3bea3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3bea3-102">SYNOPSIS</span></span>
<span data-ttu-id="3bea3-103">取得應用程式。</span><span class="sxs-lookup"><span data-stu-id="3bea3-103">Get an application.</span></span>

## <span data-ttu-id="3bea3-104">語法</span><span class="sxs-lookup"><span data-stu-id="3bea3-104">SYNTAX</span></span>

### <span data-ttu-id="3bea3-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="3bea3-105">List (Default)</span></span>
```
Get-AzWvdApplication -GroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3bea3-106">獲取</span><span class="sxs-lookup"><span data-stu-id="3bea3-106">Get</span></span>
```
Get-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3bea3-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3bea3-107">GetViaIdentity</span></span>
```
Get-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3bea3-108">描述</span><span class="sxs-lookup"><span data-stu-id="3bea3-108">DESCRIPTION</span></span>
<span data-ttu-id="3bea3-109">取得應用程式。</span><span class="sxs-lookup"><span data-stu-id="3bea3-109">Get an application.</span></span>

## <span data-ttu-id="3bea3-110">例子</span><span class="sxs-lookup"><span data-stu-id="3bea3-110">EXAMPLES</span></span>

### <span data-ttu-id="3bea3-111">範例 1：按名稱取得 Windows 虛擬桌面應用程式</span><span class="sxs-lookup"><span data-stu-id="3bea3-111">Example 1: Get a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="3bea3-112">此命令會以應用程式群組中的 Windows 虛擬桌面應用程式。</span><span class="sxs-lookup"><span data-stu-id="3bea3-112">This command gets a Windows Virtual Desktop Application in an applicaton Group.</span></span>

### <span data-ttu-id="3bea3-113">範例 2：列出 Windows 虛擬桌面應用程式</span><span class="sxs-lookup"><span data-stu-id="3bea3-113">Example 2: List Windows Virtual Desktop Applications</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName1 Microsoft.DesktopVirtualization/applicationgroups/applications
ApplicationGroupName/ApplicationName2 Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="3bea3-114">此命令會列出應用程式群組中的 Windows 虛擬桌面應用程式。</span><span class="sxs-lookup"><span data-stu-id="3bea3-114">This command Lists Windows Virtual Desktop Applications in an applicaton Group.</span></span>

## <span data-ttu-id="3bea3-115">參數</span><span class="sxs-lookup"><span data-stu-id="3bea3-115">PARAMETERS</span></span>

### <span data-ttu-id="3bea3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bea3-116">-DefaultProfile</span></span>
<span data-ttu-id="3bea3-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3bea3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bea3-118">-GroupName</span><span class="sxs-lookup"><span data-stu-id="3bea3-118">-GroupName</span></span>
<span data-ttu-id="3bea3-119">應用程式組的名稱</span><span class="sxs-lookup"><span data-stu-id="3bea3-119">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bea3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3bea3-120">-InputObject</span></span>
<span data-ttu-id="3bea3-121">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3bea3-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3bea3-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="3bea3-122">-Name</span></span>
<span data-ttu-id="3bea3-123">指定應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="3bea3-123">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bea3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bea3-124">-ResourceGroupName</span></span>
<span data-ttu-id="3bea3-125">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3bea3-125">The name of the resource group.</span></span>
<span data-ttu-id="3bea3-126">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="3bea3-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3bea3-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3bea3-127">-SubscriptionId</span></span>
<span data-ttu-id="3bea3-128">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3bea3-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3bea3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bea3-129">CommonParameters</span></span>
<span data-ttu-id="3bea3-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3bea3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bea3-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3bea3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bea3-132">輸入</span><span class="sxs-lookup"><span data-stu-id="3bea3-132">INPUTS</span></span>

### <span data-ttu-id="3bea3-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="3bea3-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="3bea3-134">輸出</span><span class="sxs-lookup"><span data-stu-id="3bea3-134">OUTPUTS</span></span>

### <span data-ttu-id="3bea3-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.Api20201102Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="3bea3-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="3bea3-136">筆記</span><span class="sxs-lookup"><span data-stu-id="3bea3-136">NOTES</span></span>

<span data-ttu-id="3bea3-137">別名</span><span class="sxs-lookup"><span data-stu-id="3bea3-137">ALIASES</span></span>

<span data-ttu-id="3bea3-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="3bea3-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3bea3-139">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3bea3-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3bea3-140">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="3bea3-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3bea3-141">INPUTOBJECT： <IDesktopVirtualizationIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="3bea3-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3bea3-142">`[ApplicationGroupName <String>]`：應用程式組的名稱</span><span class="sxs-lookup"><span data-stu-id="3bea3-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="3bea3-143">`[ApplicationName <String>]`：指定應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="3bea3-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="3bea3-144">`[DesktopName <String>]`：指定桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="3bea3-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="3bea3-145">`[HostPoolName <String>]`：指定資源群組內的主機組名</span><span class="sxs-lookup"><span data-stu-id="3bea3-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="3bea3-146">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="3bea3-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3bea3-147">`[MsixPackageFullName <String>]`：指定主機多工緩衝處理程式中 MSIX 套件的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="3bea3-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="3bea3-148">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3bea3-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3bea3-149">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="3bea3-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="3bea3-150">`[SessionHostName <String>]`：指定主機集中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="3bea3-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="3bea3-151">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3bea3-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3bea3-152">`[UserSessionId <String>]`：指定工作階段主機內的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="3bea3-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="3bea3-153">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="3bea3-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="3bea3-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="3bea3-154">RELATED LINKS</span></span>


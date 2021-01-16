---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
ms.openlocfilehash: 5f2ccffd0b0ba82b215db018ee15f4e495704f15
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447860"
---
# <span data-ttu-id="f65a0-101">Get-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="f65a0-101">Get-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="f65a0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f65a0-102">SYNOPSIS</span></span>
<span data-ttu-id="f65a0-103">取得應用程式群組。</span><span class="sxs-lookup"><span data-stu-id="f65a0-103">Get an application group.</span></span>

## <span data-ttu-id="f65a0-104">句法</span><span class="sxs-lookup"><span data-stu-id="f65a0-104">SYNTAX</span></span>

### <span data-ttu-id="f65a0-105">List1 (預設) </span><span class="sxs-lookup"><span data-stu-id="f65a0-105">List1 (Default)</span></span>
```
Get-AzWvdApplicationGroup [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f65a0-106">獲取</span><span class="sxs-lookup"><span data-stu-id="f65a0-106">Get</span></span>
```
Get-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f65a0-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f65a0-107">GetViaIdentity</span></span>
```
Get-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f65a0-108">清單</span><span class="sxs-lookup"><span data-stu-id="f65a0-108">List</span></span>
```
Get-AzWvdApplicationGroup -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f65a0-109">說明</span><span class="sxs-lookup"><span data-stu-id="f65a0-109">DESCRIPTION</span></span>
<span data-ttu-id="f65a0-110">取得應用程式群組。</span><span class="sxs-lookup"><span data-stu-id="f65a0-110">Get an application group.</span></span>

## <span data-ttu-id="f65a0-111">示例</span><span class="sxs-lookup"><span data-stu-id="f65a0-111">EXAMPLES</span></span>

### <span data-ttu-id="f65a0-112">範例1：依名稱取得 Windows 虛擬桌面 ApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="f65a0-112">Example 1: Get a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="f65a0-113">這個命令會在資源群組中取得 Windows 虛擬桌面 ApplicationGroup。</span><span class="sxs-lookup"><span data-stu-id="f65a0-113">This command gets a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="f65a0-114">範例2：列出 Windows 虛擬桌面 ApplicationGroups</span><span class="sxs-lookup"><span data-stu-id="f65a0-114">Example 2: List Windows Virtual Desktop ApplicationGroups</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName

Location   Name                  Type
--------   ----                  ----
eastus     ApplicationGroupName1 Microsoft.DesktopVirtualization/applicationgroups
eastus     ApplicationGroupName2 Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="f65a0-115">這個命令會列出資源群組中的 Windows 虛擬桌面 ApplicationGroups。</span><span class="sxs-lookup"><span data-stu-id="f65a0-115">This command lists a Windows Virtual Desktop ApplicationGroups in a Resource Group.</span></span>

## <span data-ttu-id="f65a0-116">參數</span><span class="sxs-lookup"><span data-stu-id="f65a0-116">PARAMETERS</span></span>

### <span data-ttu-id="f65a0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f65a0-117">-DefaultProfile</span></span>
<span data-ttu-id="f65a0-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f65a0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f65a0-119">-篩選</span><span class="sxs-lookup"><span data-stu-id="f65a0-119">-Filter</span></span>
<span data-ttu-id="f65a0-120">OData 篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="f65a0-120">OData filter expression.</span></span>
<span data-ttu-id="f65a0-121">ApplicationGroupType 篩選的有效屬性。</span><span class="sxs-lookup"><span data-stu-id="f65a0-121">Valid properties for filtering are applicationGroupType.</span></span>

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

### <span data-ttu-id="f65a0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f65a0-122">-InputObject</span></span>
<span data-ttu-id="f65a0-123">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f65a0-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f65a0-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="f65a0-124">-Name</span></span>
<span data-ttu-id="f65a0-125">應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="f65a0-125">The name of the application group</span></span>

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

### <span data-ttu-id="f65a0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f65a0-126">-ResourceGroupName</span></span>
<span data-ttu-id="f65a0-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f65a0-127">The name of the resource group.</span></span>
<span data-ttu-id="f65a0-128">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="f65a0-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f65a0-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f65a0-129">-SubscriptionId</span></span>
<span data-ttu-id="f65a0-130">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="f65a0-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f65a0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f65a0-131">CommonParameters</span></span>
<span data-ttu-id="f65a0-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f65a0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f65a0-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f65a0-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f65a0-134">輸入</span><span class="sxs-lookup"><span data-stu-id="f65a0-134">INPUTS</span></span>

### <span data-ttu-id="f65a0-135">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="f65a0-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="f65a0-136">輸出</span><span class="sxs-lookup"><span data-stu-id="f65a0-136">OUTPUTS</span></span>

### <span data-ttu-id="f65a0-137">IApplicationGroup （DesktopVirtualization）。 Api20201102Preview。</span><span class="sxs-lookup"><span data-stu-id="f65a0-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="f65a0-138">筆記</span><span class="sxs-lookup"><span data-stu-id="f65a0-138">NOTES</span></span>

<span data-ttu-id="f65a0-139">別名</span><span class="sxs-lookup"><span data-stu-id="f65a0-139">ALIASES</span></span>

<span data-ttu-id="f65a0-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="f65a0-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f65a0-141">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="f65a0-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f65a0-142">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="f65a0-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f65a0-143">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="f65a0-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f65a0-144">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="f65a0-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="f65a0-145">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="f65a0-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="f65a0-146">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="f65a0-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="f65a0-147">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="f65a0-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="f65a0-148">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="f65a0-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f65a0-149">`[MsixPackageFullName <String>]`： MSIX 套件在指定 hostpool 中的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="f65a0-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="f65a0-150">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f65a0-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f65a0-151">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="f65a0-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="f65a0-152">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="f65a0-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="f65a0-153">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f65a0-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f65a0-154">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="f65a0-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="f65a0-155">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="f65a0-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="f65a0-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="f65a0-156">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
ms.openlocfilehash: 8fe887f754c5a5a9f45d38d646a1edd03d1cc006
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98289215"
---
# <span data-ttu-id="a1018-101">Update-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="a1018-101">Update-AzWvdMsixPackage</span></span>

## <span data-ttu-id="a1018-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a1018-102">SYNOPSIS</span></span>
<span data-ttu-id="a1018-103">更新 MSIX 套件。</span><span class="sxs-lookup"><span data-stu-id="a1018-103">Update an  MSIX Package.</span></span>

## <span data-ttu-id="a1018-104">句法</span><span class="sxs-lookup"><span data-stu-id="a1018-104">SYNTAX</span></span>

### <span data-ttu-id="a1018-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="a1018-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DisplayName <String>] [-IsActive] [-IsRegularRegistration]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a1018-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a1018-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DisplayName <String>] [-IsActive]
 [-IsRegularRegistration] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a1018-107">說明</span><span class="sxs-lookup"><span data-stu-id="a1018-107">DESCRIPTION</span></span>
<span data-ttu-id="a1018-108">更新 MSIX 套件。</span><span class="sxs-lookup"><span data-stu-id="a1018-108">Update an  MSIX Package.</span></span>

## <span data-ttu-id="a1018-109">示例</span><span class="sxs-lookup"><span data-stu-id="a1018-109">EXAMPLES</span></span>

### <span data-ttu-id="a1018-110">範例1：更新 MSIX 套件</span><span class="sxs-lookup"><span data-stu-id="a1018-110">Example 1: Update a MSIX Package</span></span> 
```powershell
PS C:\> Update-AzWvdMsixPackage -HostPoolName HostPoolName `
                -ResourceGroupName ResourceGroupName `
                -SubscriptionId SubscriptionId `
                -displayName 'Updated-display-Name' `
                    -IsRegularRegistration:$False `
                -IsActive:$True

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName1                    Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="a1018-111">這個命令會更新 HostPool 中的 MSIX 套件。</span><span class="sxs-lookup"><span data-stu-id="a1018-111">This command updates a MSIX Package in a HostPool.</span></span>

## <span data-ttu-id="a1018-112">參數</span><span class="sxs-lookup"><span data-stu-id="a1018-112">PARAMETERS</span></span>

### <span data-ttu-id="a1018-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1018-113">-DefaultProfile</span></span>
<span data-ttu-id="a1018-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a1018-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1018-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a1018-115">-DisplayName</span></span>
<span data-ttu-id="a1018-116">MSIX 套件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a1018-116">Display name for MSIX Package.</span></span>

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

### <span data-ttu-id="a1018-117">-FullName</span><span class="sxs-lookup"><span data-stu-id="a1018-117">-FullName</span></span>
<span data-ttu-id="a1018-118">指定 hostpool 中 MSIX 套件的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="a1018-118">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1018-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="a1018-119">-HostPoolName</span></span>
<span data-ttu-id="a1018-120">指定資源群組中主機池的名稱</span><span class="sxs-lookup"><span data-stu-id="a1018-120">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1018-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1018-121">-InputObject</span></span>
<span data-ttu-id="a1018-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a1018-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1018-123">-IsActive</span><span class="sxs-lookup"><span data-stu-id="a1018-123">-IsActive</span></span>
<span data-ttu-id="a1018-124">在 hostpool 中設定要作用中的套件版本。</span><span class="sxs-lookup"><span data-stu-id="a1018-124">Set a version of the package to be active across hostpool.</span></span>

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

### <span data-ttu-id="a1018-125">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="a1018-125">-IsRegularRegistration</span></span>
<span data-ttu-id="a1018-126">設定註冊模式。</span><span class="sxs-lookup"><span data-stu-id="a1018-126">Set Registration mode.</span></span>
<span data-ttu-id="a1018-127">常規或延遲。</span><span class="sxs-lookup"><span data-stu-id="a1018-127">Regular or Delayed.</span></span>

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

### <span data-ttu-id="a1018-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1018-128">-ResourceGroupName</span></span>
<span data-ttu-id="a1018-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1018-129">The name of the resource group.</span></span>
<span data-ttu-id="a1018-130">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a1018-130">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1018-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a1018-131">-SubscriptionId</span></span>
<span data-ttu-id="a1018-132">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="a1018-132">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1018-133">-確認</span><span class="sxs-lookup"><span data-stu-id="a1018-133">-Confirm</span></span>
<span data-ttu-id="a1018-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a1018-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1018-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1018-135">-WhatIf</span></span>
<span data-ttu-id="a1018-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a1018-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1018-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a1018-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1018-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1018-138">CommonParameters</span></span>
<span data-ttu-id="a1018-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a1018-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1018-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a1018-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1018-141">輸入</span><span class="sxs-lookup"><span data-stu-id="a1018-141">INPUTS</span></span>

### <span data-ttu-id="a1018-142">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="a1018-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="a1018-143">輸出</span><span class="sxs-lookup"><span data-stu-id="a1018-143">OUTPUTS</span></span>

### <span data-ttu-id="a1018-144">IMsixPackage （DesktopVirtualization）。 Api20201102Preview。</span><span class="sxs-lookup"><span data-stu-id="a1018-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="a1018-145">筆記</span><span class="sxs-lookup"><span data-stu-id="a1018-145">NOTES</span></span>

<span data-ttu-id="a1018-146">別名</span><span class="sxs-lookup"><span data-stu-id="a1018-146">ALIASES</span></span>

<span data-ttu-id="a1018-147">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="a1018-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a1018-148">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="a1018-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a1018-149">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="a1018-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a1018-150">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="a1018-150">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a1018-151">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="a1018-151">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="a1018-152">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="a1018-152">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="a1018-153">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="a1018-153">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="a1018-154">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="a1018-154">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="a1018-155">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="a1018-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a1018-156">`[MsixPackageFullName <String>]`： MSIX 套件在指定 hostpool 中的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="a1018-156">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="a1018-157">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1018-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a1018-158">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a1018-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="a1018-159">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="a1018-159">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="a1018-160">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a1018-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a1018-161">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="a1018-161">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="a1018-162">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="a1018-162">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="a1018-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1018-163">RELATED LINKS</span></span>


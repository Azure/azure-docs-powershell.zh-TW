---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
ms.openlocfilehash: b47e87ef781138dabe5b2327227ee17f29e5a494
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274904"
---
# <span data-ttu-id="fc872-101">Update-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="fc872-101">Update-AzWvdMsixPackage</span></span>

## <span data-ttu-id="fc872-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fc872-102">SYNOPSIS</span></span>
<span data-ttu-id="fc872-103">更新 MSIX 套件。</span><span class="sxs-lookup"><span data-stu-id="fc872-103">Update an  MSIX Package.</span></span>

## <span data-ttu-id="fc872-104">句法</span><span class="sxs-lookup"><span data-stu-id="fc872-104">SYNTAX</span></span>

### <span data-ttu-id="fc872-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="fc872-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DisplayName <String>] [-IsActive] [-IsRegularRegistration]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fc872-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="fc872-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DisplayName <String>] [-IsActive]
 [-IsRegularRegistration] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fc872-107">說明</span><span class="sxs-lookup"><span data-stu-id="fc872-107">DESCRIPTION</span></span>
<span data-ttu-id="fc872-108">更新 MSIX 套件。</span><span class="sxs-lookup"><span data-stu-id="fc872-108">Update an  MSIX Package.</span></span>

## <span data-ttu-id="fc872-109">示例</span><span class="sxs-lookup"><span data-stu-id="fc872-109">EXAMPLES</span></span>

### <span data-ttu-id="fc872-110">範例1：更新 MSIX 套件</span><span class="sxs-lookup"><span data-stu-id="fc872-110">Example 1: Update a MSIX Package</span></span> 
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

<span data-ttu-id="fc872-111">這個命令會更新 HostPool 中的 MSIX 套件。</span><span class="sxs-lookup"><span data-stu-id="fc872-111">This command updates a MSIX Package in a HostPool.</span></span>

## <span data-ttu-id="fc872-112">參數</span><span class="sxs-lookup"><span data-stu-id="fc872-112">PARAMETERS</span></span>

### <span data-ttu-id="fc872-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc872-113">-DefaultProfile</span></span>
<span data-ttu-id="fc872-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fc872-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc872-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fc872-115">-DisplayName</span></span>
<span data-ttu-id="fc872-116">MSIX 套件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="fc872-116">Display name for MSIX Package.</span></span>

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

### <span data-ttu-id="fc872-117">-FullName</span><span class="sxs-lookup"><span data-stu-id="fc872-117">-FullName</span></span>
<span data-ttu-id="fc872-118">指定 hostpool 中 MSIX 套件的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="fc872-118">The version specific package full name of the MSIX package within specified hostpool</span></span>

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

### <span data-ttu-id="fc872-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="fc872-119">-HostPoolName</span></span>
<span data-ttu-id="fc872-120">指定資源群組中主機池的名稱</span><span class="sxs-lookup"><span data-stu-id="fc872-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="fc872-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc872-121">-InputObject</span></span>
<span data-ttu-id="fc872-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="fc872-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fc872-123">-IsActive</span><span class="sxs-lookup"><span data-stu-id="fc872-123">-IsActive</span></span>
<span data-ttu-id="fc872-124">在 hostpool 中設定要作用中的套件版本。</span><span class="sxs-lookup"><span data-stu-id="fc872-124">Set a version of the package to be active across hostpool.</span></span>

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

### <span data-ttu-id="fc872-125">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="fc872-125">-IsRegularRegistration</span></span>
<span data-ttu-id="fc872-126">設定註冊模式。</span><span class="sxs-lookup"><span data-stu-id="fc872-126">Set Registration mode.</span></span>
<span data-ttu-id="fc872-127">常規或延遲。</span><span class="sxs-lookup"><span data-stu-id="fc872-127">Regular or Delayed.</span></span>

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

### <span data-ttu-id="fc872-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc872-128">-ResourceGroupName</span></span>
<span data-ttu-id="fc872-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fc872-129">The name of the resource group.</span></span>
<span data-ttu-id="fc872-130">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="fc872-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fc872-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fc872-131">-SubscriptionId</span></span>
<span data-ttu-id="fc872-132">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="fc872-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fc872-133">-確認</span><span class="sxs-lookup"><span data-stu-id="fc872-133">-Confirm</span></span>
<span data-ttu-id="fc872-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fc872-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc872-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc872-135">-WhatIf</span></span>
<span data-ttu-id="fc872-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fc872-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc872-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fc872-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc872-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc872-138">CommonParameters</span></span>
<span data-ttu-id="fc872-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fc872-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc872-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fc872-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc872-141">輸入</span><span class="sxs-lookup"><span data-stu-id="fc872-141">INPUTS</span></span>

### <span data-ttu-id="fc872-142">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="fc872-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="fc872-143">輸出</span><span class="sxs-lookup"><span data-stu-id="fc872-143">OUTPUTS</span></span>

### <span data-ttu-id="fc872-144">IMsixPackage （DesktopVirtualization）。 Api20201019Preview。</span><span class="sxs-lookup"><span data-stu-id="fc872-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackage</span></span>

## <span data-ttu-id="fc872-145">筆記</span><span class="sxs-lookup"><span data-stu-id="fc872-145">NOTES</span></span>

<span data-ttu-id="fc872-146">別名</span><span class="sxs-lookup"><span data-stu-id="fc872-146">ALIASES</span></span>

<span data-ttu-id="fc872-147">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="fc872-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fc872-148">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="fc872-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fc872-149">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="fc872-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fc872-150">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="fc872-150">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fc872-151">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="fc872-151">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="fc872-152">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="fc872-152">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="fc872-153">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="fc872-153">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="fc872-154">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="fc872-154">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="fc872-155">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="fc872-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fc872-156">`[MsixPackageFullName <String>]`： MSIX 套件在指定 hostpool 中的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="fc872-156">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="fc872-157">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fc872-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="fc872-158">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="fc872-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="fc872-159">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="fc872-159">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="fc872-160">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fc872-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="fc872-161">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="fc872-161">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="fc872-162">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="fc872-162">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="fc872-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc872-163">RELATED LINKS</span></span>


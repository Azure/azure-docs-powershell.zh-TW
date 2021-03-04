---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
ms.openlocfilehash: 942b0cc6dc00d80eb56748de09c8818045dfca40
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909065"
---
# <span data-ttu-id="b58ae-101">Get-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="b58ae-101">Get-AzWvdMsixPackage</span></span>

## <span data-ttu-id="b58ae-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b58ae-102">SYNOPSIS</span></span>
<span data-ttu-id="b58ae-103">取得 msixpackage。</span><span class="sxs-lookup"><span data-stu-id="b58ae-103">Get a msixpackage.</span></span>

## <span data-ttu-id="b58ae-104">語法</span><span class="sxs-lookup"><span data-stu-id="b58ae-104">SYNTAX</span></span>

### <span data-ttu-id="b58ae-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="b58ae-105">List (Default)</span></span>
```
Get-AzWvdMsixPackage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b58ae-106">獲取</span><span class="sxs-lookup"><span data-stu-id="b58ae-106">Get</span></span>
```
Get-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b58ae-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b58ae-107">GetViaIdentity</span></span>
```
Get-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b58ae-108">描述</span><span class="sxs-lookup"><span data-stu-id="b58ae-108">DESCRIPTION</span></span>
<span data-ttu-id="b58ae-109">取得 msixpackage。</span><span class="sxs-lookup"><span data-stu-id="b58ae-109">Get a msixpackage.</span></span>

## <span data-ttu-id="b58ae-110">例子</span><span class="sxs-lookup"><span data-stu-id="b58ae-110">EXAMPLES</span></span>

### <span data-ttu-id="b58ae-111">範例 1：按名稱取得 MSIX 套件</span><span class="sxs-lookup"><span data-stu-id="b58ae-111">Example 1: Get a MSIX Package by Name</span></span>
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName                     Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="b58ae-112">此命令在 HostPool 中會獲得 MSIX 套件。</span><span class="sxs-lookup"><span data-stu-id="b58ae-112">This command gets a MSIX Package in a HostPool.</span></span>

### <span data-ttu-id="b58ae-113">範例 2：列出 MSIX 套件</span><span class="sxs-lookup"><span data-stu-id="b58ae-113">Example 2: List MSIX Packages</span></span> 
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName1                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName2                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName3                    Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="b58ae-114">此命令會列出 HostPool 中的 MSIX 套件。</span><span class="sxs-lookup"><span data-stu-id="b58ae-114">This command Lists MSIX Packages in a HostPool.</span></span>

## <span data-ttu-id="b58ae-115">參數</span><span class="sxs-lookup"><span data-stu-id="b58ae-115">PARAMETERS</span></span>

### <span data-ttu-id="b58ae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b58ae-116">-DefaultProfile</span></span>
<span data-ttu-id="b58ae-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b58ae-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b58ae-118">-FullName</span><span class="sxs-lookup"><span data-stu-id="b58ae-118">-FullName</span></span>
<span data-ttu-id="b58ae-119">指定主機多工緩衝處理程式中 MSIX 套件的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="b58ae-119">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b58ae-120">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="b58ae-120">-HostPoolName</span></span>
<span data-ttu-id="b58ae-121">指定資源群組內的主機組名</span><span class="sxs-lookup"><span data-stu-id="b58ae-121">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="b58ae-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b58ae-122">-InputObject</span></span>
<span data-ttu-id="b58ae-123">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b58ae-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b58ae-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b58ae-124">-ResourceGroupName</span></span>
<span data-ttu-id="b58ae-125">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b58ae-125">The name of the resource group.</span></span>
<span data-ttu-id="b58ae-126">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b58ae-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b58ae-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b58ae-127">-SubscriptionId</span></span>
<span data-ttu-id="b58ae-128">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b58ae-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b58ae-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b58ae-129">CommonParameters</span></span>
<span data-ttu-id="b58ae-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b58ae-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b58ae-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b58ae-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b58ae-132">輸入</span><span class="sxs-lookup"><span data-stu-id="b58ae-132">INPUTS</span></span>

### <span data-ttu-id="b58ae-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="b58ae-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="b58ae-134">輸出</span><span class="sxs-lookup"><span data-stu-id="b58ae-134">OUTPUTS</span></span>

### <span data-ttu-id="b58ae-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.Api20201102Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="b58ae-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="b58ae-136">筆記</span><span class="sxs-lookup"><span data-stu-id="b58ae-136">NOTES</span></span>

<span data-ttu-id="b58ae-137">別名</span><span class="sxs-lookup"><span data-stu-id="b58ae-137">ALIASES</span></span>

<span data-ttu-id="b58ae-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="b58ae-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b58ae-139">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b58ae-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b58ae-140">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b58ae-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b58ae-141">INPUTOBJECT： <IDesktopVirtualizationIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="b58ae-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b58ae-142">`[ApplicationGroupName <String>]`：應用程式組的名稱</span><span class="sxs-lookup"><span data-stu-id="b58ae-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="b58ae-143">`[ApplicationName <String>]`：指定應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="b58ae-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="b58ae-144">`[DesktopName <String>]`：指定桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="b58ae-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="b58ae-145">`[HostPoolName <String>]`：指定資源群組內的主機組名</span><span class="sxs-lookup"><span data-stu-id="b58ae-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="b58ae-146">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="b58ae-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b58ae-147">`[MsixPackageFullName <String>]`：指定主機多工緩衝處理程式中 MSIX 套件的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="b58ae-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="b58ae-148">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b58ae-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b58ae-149">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b58ae-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="b58ae-150">`[SessionHostName <String>]`：指定主機集中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="b58ae-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="b58ae-151">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b58ae-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b58ae-152">`[UserSessionId <String>]`：指定工作階段主機內的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="b58ae-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="b58ae-153">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="b58ae-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="b58ae-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="b58ae-154">RELATED LINKS</span></span>


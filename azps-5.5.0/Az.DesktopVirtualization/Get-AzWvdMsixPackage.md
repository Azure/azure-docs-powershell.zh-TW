---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
ms.openlocfilehash: 51b940df2ee26c3da53c34fd7f1ffa25d3a266a9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139270"
---
# <span data-ttu-id="38a31-101">Get-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="38a31-101">Get-AzWvdMsixPackage</span></span>

## <span data-ttu-id="38a31-102">摘要</span><span class="sxs-lookup"><span data-stu-id="38a31-102">SYNOPSIS</span></span>
<span data-ttu-id="38a31-103">取得 msixpackage。</span><span class="sxs-lookup"><span data-stu-id="38a31-103">Get a msixpackage.</span></span>

## <span data-ttu-id="38a31-104">句法</span><span class="sxs-lookup"><span data-stu-id="38a31-104">SYNTAX</span></span>

### <span data-ttu-id="38a31-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="38a31-105">List (Default)</span></span>
```
Get-AzWvdMsixPackage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="38a31-106">獲取</span><span class="sxs-lookup"><span data-stu-id="38a31-106">Get</span></span>
```
Get-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="38a31-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="38a31-107">GetViaIdentity</span></span>
```
Get-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="38a31-108">說明</span><span class="sxs-lookup"><span data-stu-id="38a31-108">DESCRIPTION</span></span>
<span data-ttu-id="38a31-109">取得 msixpackage。</span><span class="sxs-lookup"><span data-stu-id="38a31-109">Get a msixpackage.</span></span>

## <span data-ttu-id="38a31-110">示例</span><span class="sxs-lookup"><span data-stu-id="38a31-110">EXAMPLES</span></span>

### <span data-ttu-id="38a31-111">範例1：依名稱取得 MSIX 套件</span><span class="sxs-lookup"><span data-stu-id="38a31-111">Example 1: Get a MSIX Package by Name</span></span>
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName                     Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="38a31-112">這個命令會在 HostPool 中取得 MSIX 套件。</span><span class="sxs-lookup"><span data-stu-id="38a31-112">This command gets a MSIX Package in a HostPool.</span></span>

### <span data-ttu-id="38a31-113">範例2：清單 MSIX 套件</span><span class="sxs-lookup"><span data-stu-id="38a31-113">Example 2: List MSIX Packages</span></span> 
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName1                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName2                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName3                    Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="38a31-114">這個命令會列出 HostPool 中的 MSIX 套件。</span><span class="sxs-lookup"><span data-stu-id="38a31-114">This command Lists MSIX Packages in a HostPool.</span></span>

## <span data-ttu-id="38a31-115">參數</span><span class="sxs-lookup"><span data-stu-id="38a31-115">PARAMETERS</span></span>

### <span data-ttu-id="38a31-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38a31-116">-DefaultProfile</span></span>
<span data-ttu-id="38a31-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="38a31-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38a31-118">-FullName</span><span class="sxs-lookup"><span data-stu-id="38a31-118">-FullName</span></span>
<span data-ttu-id="38a31-119">指定 hostpool 中 MSIX 套件的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="38a31-119">The version specific package full name of the MSIX package within specified hostpool</span></span>

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

### <span data-ttu-id="38a31-120">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="38a31-120">-HostPoolName</span></span>
<span data-ttu-id="38a31-121">指定資源群組中主機池的名稱</span><span class="sxs-lookup"><span data-stu-id="38a31-121">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="38a31-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38a31-122">-InputObject</span></span>
<span data-ttu-id="38a31-123">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="38a31-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="38a31-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38a31-124">-ResourceGroupName</span></span>
<span data-ttu-id="38a31-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="38a31-125">The name of the resource group.</span></span>
<span data-ttu-id="38a31-126">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="38a31-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="38a31-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="38a31-127">-SubscriptionId</span></span>
<span data-ttu-id="38a31-128">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="38a31-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="38a31-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38a31-129">CommonParameters</span></span>
<span data-ttu-id="38a31-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="38a31-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38a31-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="38a31-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38a31-132">輸入</span><span class="sxs-lookup"><span data-stu-id="38a31-132">INPUTS</span></span>

### <span data-ttu-id="38a31-133">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="38a31-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="38a31-134">輸出</span><span class="sxs-lookup"><span data-stu-id="38a31-134">OUTPUTS</span></span>

### <span data-ttu-id="38a31-135">IMsixPackage （DesktopVirtualization）。 Api20201102Preview。</span><span class="sxs-lookup"><span data-stu-id="38a31-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="38a31-136">筆記</span><span class="sxs-lookup"><span data-stu-id="38a31-136">NOTES</span></span>

<span data-ttu-id="38a31-137">別名</span><span class="sxs-lookup"><span data-stu-id="38a31-137">ALIASES</span></span>

<span data-ttu-id="38a31-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="38a31-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="38a31-139">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="38a31-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="38a31-140">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="38a31-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="38a31-141">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="38a31-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="38a31-142">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="38a31-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="38a31-143">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="38a31-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="38a31-144">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="38a31-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="38a31-145">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="38a31-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="38a31-146">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="38a31-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="38a31-147">`[MsixPackageFullName <String>]`： MSIX 套件在指定 hostpool 中的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="38a31-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="38a31-148">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="38a31-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="38a31-149">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="38a31-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="38a31-150">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="38a31-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="38a31-151">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="38a31-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="38a31-152">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="38a31-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="38a31-153">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="38a31-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="38a31-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="38a31-154">RELATED LINKS</span></span>


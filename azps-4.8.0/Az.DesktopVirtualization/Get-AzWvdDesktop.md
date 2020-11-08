---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
ms.openlocfilehash: 72075a00cab24d9e7ac82814b2f1e644d90d74c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971117"
---
# <span data-ttu-id="31f57-101">Get-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="31f57-101">Get-AzWvdDesktop</span></span>

## <span data-ttu-id="31f57-102">摘要</span><span class="sxs-lookup"><span data-stu-id="31f57-102">SYNOPSIS</span></span>
<span data-ttu-id="31f57-103">取得桌面。</span><span class="sxs-lookup"><span data-stu-id="31f57-103">Get a desktop.</span></span>

## <span data-ttu-id="31f57-104">句法</span><span class="sxs-lookup"><span data-stu-id="31f57-104">SYNTAX</span></span>

### <span data-ttu-id="31f57-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="31f57-105">List (Default)</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="31f57-106">獲取</span><span class="sxs-lookup"><span data-stu-id="31f57-106">Get</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="31f57-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="31f57-107">GetViaIdentity</span></span>
```
Get-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="31f57-108">說明</span><span class="sxs-lookup"><span data-stu-id="31f57-108">DESCRIPTION</span></span>
<span data-ttu-id="31f57-109">取得桌面。</span><span class="sxs-lookup"><span data-stu-id="31f57-109">Get a desktop.</span></span>

## <span data-ttu-id="31f57-110">示例</span><span class="sxs-lookup"><span data-stu-id="31f57-110">EXAMPLES</span></span>

### <span data-ttu-id="31f57-111">範例1：依名稱取得 Windows 虛擬桌面電腦桌面</span><span class="sxs-lookup"><span data-stu-id="31f57-111">Example 1: Get a Windows Virtual Desktop Desktop by name</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name DesktopName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="31f57-112">這個命令會在 applicaton 群組中取得 Windows 虛擬桌面電腦。</span><span class="sxs-lookup"><span data-stu-id="31f57-112">This command gets a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

### <span data-ttu-id="31f57-113">範例2：列出 Windows 虛擬桌面桌面</span><span class="sxs-lookup"><span data-stu-id="31f57-113">Example 2: List Windows Virtual Desktop Desktops</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="31f57-114">此命令會 listsWindows applicaton 群組中的虛擬桌面電腦。</span><span class="sxs-lookup"><span data-stu-id="31f57-114">This command listsWindows Virtual Desktop Desktops in an applicaton Group.</span></span>

## <span data-ttu-id="31f57-115">參數</span><span class="sxs-lookup"><span data-stu-id="31f57-115">PARAMETERS</span></span>

### <span data-ttu-id="31f57-116">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="31f57-116">-ApplicationGroupName</span></span>
<span data-ttu-id="31f57-117">應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="31f57-117">The name of the application group</span></span>

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

### <span data-ttu-id="31f57-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31f57-118">-DefaultProfile</span></span>
<span data-ttu-id="31f57-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="31f57-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31f57-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31f57-120">-InputObject</span></span>
<span data-ttu-id="31f57-121">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="31f57-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="31f57-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="31f57-122">-Name</span></span>
<span data-ttu-id="31f57-123">指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="31f57-123">The name of the desktop within the specified desktop group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DesktopName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f57-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31f57-124">-ResourceGroupName</span></span>
<span data-ttu-id="31f57-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="31f57-125">The name of the resource group.</span></span>
<span data-ttu-id="31f57-126">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="31f57-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="31f57-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="31f57-127">-SubscriptionId</span></span>
<span data-ttu-id="31f57-128">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="31f57-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="31f57-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31f57-129">CommonParameters</span></span>
<span data-ttu-id="31f57-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="31f57-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31f57-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="31f57-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31f57-132">輸入</span><span class="sxs-lookup"><span data-stu-id="31f57-132">INPUTS</span></span>

### <span data-ttu-id="31f57-133">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="31f57-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="31f57-134">輸出</span><span class="sxs-lookup"><span data-stu-id="31f57-134">OUTPUTS</span></span>

### <span data-ttu-id="31f57-135">IDesktop （DesktopVirtualization）。 Api20191210Preview。</span><span class="sxs-lookup"><span data-stu-id="31f57-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IDesktop</span></span>

### <span data-ttu-id="31f57-136">IDesktopList （DesktopVirtualization）。 Api20191210Preview。</span><span class="sxs-lookup"><span data-stu-id="31f57-136">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IDesktopList</span></span>

## <span data-ttu-id="31f57-137">筆記</span><span class="sxs-lookup"><span data-stu-id="31f57-137">NOTES</span></span>

<span data-ttu-id="31f57-138">別名</span><span class="sxs-lookup"><span data-stu-id="31f57-138">ALIASES</span></span>

<span data-ttu-id="31f57-139">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="31f57-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="31f57-140">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="31f57-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="31f57-141">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="31f57-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="31f57-142">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="31f57-142">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="31f57-143">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="31f57-143">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="31f57-144">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="31f57-144">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="31f57-145">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="31f57-145">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="31f57-146">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="31f57-146">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="31f57-147">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="31f57-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="31f57-148">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="31f57-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="31f57-149">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="31f57-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="31f57-150">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="31f57-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="31f57-151">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="31f57-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="31f57-152">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="31f57-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="31f57-153">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="31f57-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="31f57-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="31f57-154">RELATED LINKS</span></span>


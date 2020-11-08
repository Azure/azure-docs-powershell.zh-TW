---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
ms.openlocfilehash: e04d13b96f36b96b2ae1c22f6f6e5b3c50b338f4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128736"
---
# <span data-ttu-id="3cbb1-101">Get-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="3cbb1-101">Get-AzWvdHostPool</span></span>

## <span data-ttu-id="3cbb1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3cbb1-102">SYNOPSIS</span></span>
<span data-ttu-id="3cbb1-103">取得主機池。</span><span class="sxs-lookup"><span data-stu-id="3cbb1-103">Get a host pool.</span></span>

## <span data-ttu-id="3cbb1-104">句法</span><span class="sxs-lookup"><span data-stu-id="3cbb1-104">SYNTAX</span></span>

### <span data-ttu-id="3cbb1-105">List1 (預設) </span><span class="sxs-lookup"><span data-stu-id="3cbb1-105">List1 (Default)</span></span>
```
Get-AzWvdHostPool [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3cbb1-106">獲取</span><span class="sxs-lookup"><span data-stu-id="3cbb1-106">Get</span></span>
```
Get-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3cbb1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3cbb1-107">GetViaIdentity</span></span>
```
Get-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="3cbb1-108">清單</span><span class="sxs-lookup"><span data-stu-id="3cbb1-108">List</span></span>
```
Get-AzWvdHostPool -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3cbb1-109">說明</span><span class="sxs-lookup"><span data-stu-id="3cbb1-109">DESCRIPTION</span></span>
<span data-ttu-id="3cbb1-110">取得主機池。</span><span class="sxs-lookup"><span data-stu-id="3cbb1-110">Get a host pool.</span></span>

## <span data-ttu-id="3cbb1-111">示例</span><span class="sxs-lookup"><span data-stu-id="3cbb1-111">EXAMPLES</span></span>

### <span data-ttu-id="3cbb1-112">範例1：依名稱取得 Windows 虛擬桌面 HostPool</span><span class="sxs-lookup"><span data-stu-id="3cbb1-112">Example 1: Get a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="3cbb1-113">這個命令會在資源群組中取得 Windows 虛擬桌面 HostPool。</span><span class="sxs-lookup"><span data-stu-id="3cbb1-113">This command gets a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="3cbb1-114">範例2：列出 Windows 虛擬桌面 HostPools</span><span class="sxs-lookup"><span data-stu-id="3cbb1-114">Example 2: List Windows Virtual Desktop HostPools</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName

Location   Name          Type
--------   ----          ----
eastus     HostPoolName1 Microsoft.DesktopVirtualization/hostpools
eastus     HostPoolName2 Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="3cbb1-115">這個命令會列出資源群組中的 Windows 虛擬桌面 HostPools。</span><span class="sxs-lookup"><span data-stu-id="3cbb1-115">This command lists a Windows Virtual Desktop HostPools in a Resource Group.</span></span>

## <span data-ttu-id="3cbb1-116">參數</span><span class="sxs-lookup"><span data-stu-id="3cbb1-116">PARAMETERS</span></span>

### <span data-ttu-id="3cbb1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cbb1-117">-DefaultProfile</span></span>
<span data-ttu-id="3cbb1-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3cbb1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cbb1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3cbb1-119">-InputObject</span></span>
<span data-ttu-id="3cbb1-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3cbb1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3cbb1-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="3cbb1-121">-Name</span></span>
<span data-ttu-id="3cbb1-122">指定資源群組中主機池的名稱</span><span class="sxs-lookup"><span data-stu-id="3cbb1-122">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cbb1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cbb1-123">-ResourceGroupName</span></span>
<span data-ttu-id="3cbb1-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3cbb1-124">The name of the resource group.</span></span>
<span data-ttu-id="3cbb1-125">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="3cbb1-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3cbb1-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3cbb1-126">-SubscriptionId</span></span>
<span data-ttu-id="3cbb1-127">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="3cbb1-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3cbb1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cbb1-128">CommonParameters</span></span>
<span data-ttu-id="3cbb1-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3cbb1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cbb1-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3cbb1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cbb1-131">輸入</span><span class="sxs-lookup"><span data-stu-id="3cbb1-131">INPUTS</span></span>

### <span data-ttu-id="3cbb1-132">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="3cbb1-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="3cbb1-133">輸出</span><span class="sxs-lookup"><span data-stu-id="3cbb1-133">OUTPUTS</span></span>

### <span data-ttu-id="3cbb1-134">IHostPool （DesktopVirtualization）。 Api20191210Preview。</span><span class="sxs-lookup"><span data-stu-id="3cbb1-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IHostPool</span></span>

## <span data-ttu-id="3cbb1-135">筆記</span><span class="sxs-lookup"><span data-stu-id="3cbb1-135">NOTES</span></span>

<span data-ttu-id="3cbb1-136">別名</span><span class="sxs-lookup"><span data-stu-id="3cbb1-136">ALIASES</span></span>

<span data-ttu-id="3cbb1-137">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="3cbb1-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3cbb1-138">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="3cbb1-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3cbb1-139">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="3cbb1-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3cbb1-140">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="3cbb1-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3cbb1-141">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="3cbb1-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="3cbb1-142">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="3cbb1-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="3cbb1-143">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="3cbb1-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="3cbb1-144">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="3cbb1-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="3cbb1-145">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="3cbb1-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3cbb1-146">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3cbb1-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3cbb1-147">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="3cbb1-147">The name is case insensitive.</span></span>
  - <span data-ttu-id="3cbb1-148">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="3cbb1-148">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="3cbb1-149">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3cbb1-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3cbb1-150">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="3cbb1-150">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="3cbb1-151">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="3cbb1-151">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="3cbb1-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="3cbb1-152">RELATED LINKS</span></span>

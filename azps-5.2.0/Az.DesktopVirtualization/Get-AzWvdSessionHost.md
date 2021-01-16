---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
ms.openlocfilehash: 806bd45ca4a9c3332388214ef146772c19282355
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275527"
---
# <span data-ttu-id="11856-101">Get-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="11856-101">Get-AzWvdSessionHost</span></span>

## <span data-ttu-id="11856-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11856-102">SYNOPSIS</span></span>
<span data-ttu-id="11856-103">取得工作階段主機。</span><span class="sxs-lookup"><span data-stu-id="11856-103">Get a session host.</span></span>

## <span data-ttu-id="11856-104">句法</span><span class="sxs-lookup"><span data-stu-id="11856-104">SYNTAX</span></span>

### <span data-ttu-id="11856-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="11856-105">List (Default)</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="11856-106">獲取</span><span class="sxs-lookup"><span data-stu-id="11856-106">Get</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="11856-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="11856-107">GetViaIdentity</span></span>
```
Get-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="11856-108">說明</span><span class="sxs-lookup"><span data-stu-id="11856-108">DESCRIPTION</span></span>
<span data-ttu-id="11856-109">取得工作階段主機。</span><span class="sxs-lookup"><span data-stu-id="11856-109">Get a session host.</span></span>

## <span data-ttu-id="11856-110">示例</span><span class="sxs-lookup"><span data-stu-id="11856-110">EXAMPLES</span></span>

### <span data-ttu-id="11856-111">範例1：依名稱取得 Windows 虛擬桌面 SessionHost</span><span class="sxs-lookup"><span data-stu-id="11856-111">Example 1: Get a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="11856-112">這個命令會在主機池中取得 Windows 虛擬桌面 SessionHost。</span><span class="sxs-lookup"><span data-stu-id="11856-112">This command gets a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

### <span data-ttu-id="11856-113">範例2：列出 Windows 虛擬桌面 SessionHosts</span><span class="sxs-lookup"><span data-stu-id="11856-113">Example 2: List Windows Virtual Desktop SessionHosts</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName1 Microsoft.DesktopVirtualization/hostpools/sessionhosts
HostPoolName/SessionHostName2 Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="11856-114">這個命令會在主機池中列出 Windows 虛擬桌面 SessionHosts。</span><span class="sxs-lookup"><span data-stu-id="11856-114">This command lists a Windows Virtual Desktop SessionHosts in a Host Pool.</span></span>

## <span data-ttu-id="11856-115">參數</span><span class="sxs-lookup"><span data-stu-id="11856-115">PARAMETERS</span></span>

### <span data-ttu-id="11856-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11856-116">-DefaultProfile</span></span>
<span data-ttu-id="11856-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="11856-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11856-118">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="11856-118">-HostPoolName</span></span>
<span data-ttu-id="11856-119">指定資源群組中主機池的名稱</span><span class="sxs-lookup"><span data-stu-id="11856-119">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="11856-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11856-120">-InputObject</span></span>
<span data-ttu-id="11856-121">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="11856-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="11856-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="11856-122">-Name</span></span>
<span data-ttu-id="11856-123">指定主機池中工作階段主機的名稱</span><span class="sxs-lookup"><span data-stu-id="11856-123">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11856-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11856-124">-ResourceGroupName</span></span>
<span data-ttu-id="11856-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="11856-125">The name of the resource group.</span></span>
<span data-ttu-id="11856-126">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="11856-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="11856-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="11856-127">-SubscriptionId</span></span>
<span data-ttu-id="11856-128">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="11856-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="11856-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11856-129">CommonParameters</span></span>
<span data-ttu-id="11856-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="11856-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11856-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="11856-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11856-132">輸入</span><span class="sxs-lookup"><span data-stu-id="11856-132">INPUTS</span></span>

### <span data-ttu-id="11856-133">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="11856-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="11856-134">輸出</span><span class="sxs-lookup"><span data-stu-id="11856-134">OUTPUTS</span></span>

### <span data-ttu-id="11856-135">ISessionHost （DesktopVirtualization）。 Api20201019Preview。</span><span class="sxs-lookup"><span data-stu-id="11856-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.ISessionHost</span></span>

## <span data-ttu-id="11856-136">筆記</span><span class="sxs-lookup"><span data-stu-id="11856-136">NOTES</span></span>

<span data-ttu-id="11856-137">別名</span><span class="sxs-lookup"><span data-stu-id="11856-137">ALIASES</span></span>

<span data-ttu-id="11856-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="11856-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="11856-139">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="11856-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="11856-140">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="11856-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="11856-141">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="11856-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="11856-142">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="11856-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="11856-143">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="11856-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="11856-144">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="11856-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="11856-145">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="11856-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="11856-146">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="11856-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="11856-147">`[MsixPackageFullName <String>]`： MSIX 套件在指定 hostpool 中的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="11856-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="11856-148">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="11856-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="11856-149">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="11856-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="11856-150">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="11856-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="11856-151">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="11856-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="11856-152">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="11856-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="11856-153">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="11856-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="11856-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="11856-154">RELATED LINKS</span></span>


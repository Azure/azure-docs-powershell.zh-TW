---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/get-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
ms.openlocfilehash: 88847cbb128f5545a235eb2c5c02043231ff1078
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969431"
---
# <span data-ttu-id="dbcc7-101">Get-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="dbcc7-101">Get-AzAppConfigurationStore</span></span>

## <span data-ttu-id="dbcc7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dbcc7-102">SYNOPSIS</span></span>
<span data-ttu-id="dbcc7-103">取得或列出 app 設定存放區。</span><span class="sxs-lookup"><span data-stu-id="dbcc7-103">Get or list app configuration stores.</span></span>

## <span data-ttu-id="dbcc7-104">句法</span><span class="sxs-lookup"><span data-stu-id="dbcc7-104">SYNTAX</span></span>

### <span data-ttu-id="dbcc7-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="dbcc7-105">List (Default)</span></span>
```
Get-AzAppConfigurationStore [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dbcc7-106">獲取</span><span class="sxs-lookup"><span data-stu-id="dbcc7-106">Get</span></span>
```
Get-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dbcc7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dbcc7-107">GetViaIdentity</span></span>
```
Get-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="dbcc7-108">List1</span><span class="sxs-lookup"><span data-stu-id="dbcc7-108">List1</span></span>
```
Get-AzAppConfigurationStore -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="dbcc7-109">說明</span><span class="sxs-lookup"><span data-stu-id="dbcc7-109">DESCRIPTION</span></span>
<span data-ttu-id="dbcc7-110">取得或列出 app 設定存放區。</span><span class="sxs-lookup"><span data-stu-id="dbcc7-110">Get or list app configuration stores.</span></span>

## <span data-ttu-id="dbcc7-111">示例</span><span class="sxs-lookup"><span data-stu-id="dbcc7-111">EXAMPLES</span></span>

### <span data-ttu-id="dbcc7-112">範例1：列出訂閱下的所有 app 設定儲存區</span><span class="sxs-lookup"><span data-stu-id="dbcc7-112">Example 1: List all app configuration stores under a subscription</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore

Location Name               Type
-------- ----               ----
eastus   appconfig-test01   Microsoft.AppConfiguration/configurationStores
eastus   contoso-app-config Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="dbcc7-113">這個命令會列出訂閱中的所有 app 設定儲存區。</span><span class="sxs-lookup"><span data-stu-id="dbcc7-113">This command lists all app configuration stores under a subscription.</span></span>

### <span data-ttu-id="dbcc7-114">範例2：在 [資源] 群組下列出所有 app 設定的儲存區</span><span class="sxs-lookup"><span data-stu-id="dbcc7-114">Example 2: List all app configuration stores under a resource group</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
eastus   appconfig-test02 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="dbcc7-115">這個命令會列出 [資源] 群組底下的所有 app 設定存儲區。</span><span class="sxs-lookup"><span data-stu-id="dbcc7-115">This command lists all app configuration stores under a resource group.</span></span>

### <span data-ttu-id="dbcc7-116">範例3：依名稱取得 app 設定儲存區</span><span class="sxs-lookup"><span data-stu-id="dbcc7-116">Example 3: Get an app configuration store by name</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="dbcc7-117">這個命令會透過名稱取得 app 設定儲存區。</span><span class="sxs-lookup"><span data-stu-id="dbcc7-117">This command gets an app configuration store by name.</span></span>

### <span data-ttu-id="dbcc7-118">範例4：透過管線取得 app 設定儲存區</span><span class="sxs-lookup"><span data-stu-id="dbcc7-118">Example 4: Get an app configuration store by pipeline</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01 | Get-AzAppConfigurationStore

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="dbcc7-119">這個命令會透過管線取得 app 配置存儲區。</span><span class="sxs-lookup"><span data-stu-id="dbcc7-119">This command gets an app configuration store by pipeline.</span></span>

## <span data-ttu-id="dbcc7-120">參數</span><span class="sxs-lookup"><span data-stu-id="dbcc7-120">PARAMETERS</span></span>

### <span data-ttu-id="dbcc7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbcc7-121">-DefaultProfile</span></span>
<span data-ttu-id="dbcc7-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dbcc7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbcc7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dbcc7-123">-InputObject</span></span>
<span data-ttu-id="dbcc7-124">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="dbcc7-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbcc7-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="dbcc7-125">-Name</span></span>
<span data-ttu-id="dbcc7-126">配置存放區的名稱。</span><span class="sxs-lookup"><span data-stu-id="dbcc7-126">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbcc7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbcc7-127">-ResourceGroupName</span></span>
<span data-ttu-id="dbcc7-128">容器註冊表所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dbcc7-128">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbcc7-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dbcc7-129">-SubscriptionId</span></span>
<span data-ttu-id="dbcc7-130">Microsoft Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="dbcc7-130">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="dbcc7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbcc7-131">CommonParameters</span></span>
<span data-ttu-id="dbcc7-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dbcc7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbcc7-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dbcc7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbcc7-134">輸入</span><span class="sxs-lookup"><span data-stu-id="dbcc7-134">INPUTS</span></span>

### <span data-ttu-id="dbcc7-135">IAppConfigurationIdentity （AppConfiguration）的</span><span class="sxs-lookup"><span data-stu-id="dbcc7-135">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="dbcc7-136">輸出</span><span class="sxs-lookup"><span data-stu-id="dbcc7-136">OUTPUTS</span></span>

### <span data-ttu-id="dbcc7-137">IConfigurationStore （AppConfiguration）。 Api20200601。</span><span class="sxs-lookup"><span data-stu-id="dbcc7-137">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="dbcc7-138">筆記</span><span class="sxs-lookup"><span data-stu-id="dbcc7-138">NOTES</span></span>

<span data-ttu-id="dbcc7-139">別名</span><span class="sxs-lookup"><span data-stu-id="dbcc7-139">ALIASES</span></span>

<span data-ttu-id="dbcc7-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="dbcc7-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dbcc7-141">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="dbcc7-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dbcc7-142">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="dbcc7-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dbcc7-143">INPUTOBJECT <IAppConfigurationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="dbcc7-143">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dbcc7-144">`[ConfigStoreName <String>]`：配置存放區的名稱。</span><span class="sxs-lookup"><span data-stu-id="dbcc7-144">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="dbcc7-145">`[GroupName <String>]`：私人連結資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dbcc7-145">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="dbcc7-146">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="dbcc7-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dbcc7-147">`[PrivateEndpointConnectionName <String>]`：私人端點連接名稱</span><span class="sxs-lookup"><span data-stu-id="dbcc7-147">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="dbcc7-148">`[ResourceGroupName <String>]`：容器註冊表所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dbcc7-148">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="dbcc7-149">`[SubscriptionId <String>]`： Microsoft Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="dbcc7-149">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="dbcc7-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="dbcc7-150">RELATED LINKS</span></span>

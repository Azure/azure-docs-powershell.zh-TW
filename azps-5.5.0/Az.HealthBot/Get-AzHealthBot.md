---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthbot/get-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
ms.openlocfilehash: f7e1f596aef9169a1238f505d39f0dd201dcd8bb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129306"
---
# <span data-ttu-id="aaafa-101">Get-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="aaafa-101">Get-AzHealthBot</span></span>

## <span data-ttu-id="aaafa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aaafa-102">SYNOPSIS</span></span>
<span data-ttu-id="aaafa-103">取得 HealthBot。</span><span class="sxs-lookup"><span data-stu-id="aaafa-103">Get a HealthBot.</span></span>

## <span data-ttu-id="aaafa-104">句法</span><span class="sxs-lookup"><span data-stu-id="aaafa-104">SYNTAX</span></span>

### <span data-ttu-id="aaafa-105">List1 (預設) </span><span class="sxs-lookup"><span data-stu-id="aaafa-105">List1 (Default)</span></span>
```
Get-AzHealthBot [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="aaafa-106">獲取</span><span class="sxs-lookup"><span data-stu-id="aaafa-106">Get</span></span>
```
Get-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="aaafa-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="aaafa-107">GetViaIdentity</span></span>
```
Get-AzHealthBot -InputObject <IHealthBotIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="aaafa-108">清單</span><span class="sxs-lookup"><span data-stu-id="aaafa-108">List</span></span>
```
Get-AzHealthBot -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="aaafa-109">說明</span><span class="sxs-lookup"><span data-stu-id="aaafa-109">DESCRIPTION</span></span>
<span data-ttu-id="aaafa-110">取得 HealthBot。</span><span class="sxs-lookup"><span data-stu-id="aaafa-110">Get a HealthBot.</span></span>

## <span data-ttu-id="aaafa-111">示例</span><span class="sxs-lookup"><span data-stu-id="aaafa-111">EXAMPLES</span></span>

### <span data-ttu-id="aaafa-112">範例1：取得所有 HealthBot</span><span class="sxs-lookup"><span data-stu-id="aaafa-112">Example 1: Get all HealthBot</span></span>
```powershell
PS C:\> Get-AzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="aaafa-113">取得所有 HealthBot</span><span class="sxs-lookup"><span data-stu-id="aaafa-113">Get all HealthBot</span></span>

### <span data-ttu-id="aaafa-114">範例2：透過 ResourceGroupName 取得所有 HealthBot</span><span class="sxs-lookup"><span data-stu-id="aaafa-114">Example 2: Get all HealthBot by ResourceGroupName</span></span>
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="aaafa-115">透過 ResourceGroupName 取得所有 HealthBot</span><span class="sxs-lookup"><span data-stu-id="aaafa-115">Get all HealthBot by ResourceGroupName</span></span>

### <span data-ttu-id="aaafa-116">範例3：透過 ResourceGroupName 和 Name 取得 HealthBot</span><span class="sxs-lookup"><span data-stu-id="aaafa-116">Example 3: Get HealthBot by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="aaafa-117">透過 ResourceGroupName 和名稱取得 HealthBot</span><span class="sxs-lookup"><span data-stu-id="aaafa-117">Get HealthBot by ResourceGroupName and Name</span></span>

### <span data-ttu-id="aaafa-118">範例4：透過 InputObject 取得 HealthBot</span><span class="sxs-lookup"><span data-stu-id="aaafa-118">Example 4: Get HealthBot by InputObject</span></span>
```powershell
PS C:\> $getAzHealthBot = Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot
Get-AzHealthBot -InputObject $getAzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="aaafa-119">透過 InputObject 取得 HealthBot</span><span class="sxs-lookup"><span data-stu-id="aaafa-119">Get HealthBot by InputObject</span></span>

## <span data-ttu-id="aaafa-120">參數</span><span class="sxs-lookup"><span data-stu-id="aaafa-120">PARAMETERS</span></span>

### <span data-ttu-id="aaafa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaafa-121">-DefaultProfile</span></span>
<span data-ttu-id="aaafa-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="aaafa-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaafa-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aaafa-123">-InputObject</span></span>
<span data-ttu-id="aaafa-124">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="aaafa-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aaafa-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="aaafa-125">-Name</span></span>
<span data-ttu-id="aaafa-126">Bot 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="aaafa-126">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaafa-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaafa-127">-ResourceGroupName</span></span>
<span data-ttu-id="aaafa-128">使用者訂閱中 Bot 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="aaafa-128">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="aaafa-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aaafa-129">-SubscriptionId</span></span>
<span data-ttu-id="aaafa-130">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="aaafa-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="aaafa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaafa-131">CommonParameters</span></span>
<span data-ttu-id="aaafa-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aaafa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaafa-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="aaafa-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaafa-134">輸入</span><span class="sxs-lookup"><span data-stu-id="aaafa-134">INPUTS</span></span>

### <span data-ttu-id="aaafa-135">IHealthBotIdentity （HealthBot）的</span><span class="sxs-lookup"><span data-stu-id="aaafa-135">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="aaafa-136">輸出</span><span class="sxs-lookup"><span data-stu-id="aaafa-136">OUTPUTS</span></span>

### <span data-ttu-id="aaafa-137">IHealthBot （HealthBot）。 Api20201208。</span><span class="sxs-lookup"><span data-stu-id="aaafa-137">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="aaafa-138">筆記</span><span class="sxs-lookup"><span data-stu-id="aaafa-138">NOTES</span></span>

<span data-ttu-id="aaafa-139">別名</span><span class="sxs-lookup"><span data-stu-id="aaafa-139">ALIASES</span></span>

<span data-ttu-id="aaafa-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="aaafa-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aaafa-141">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="aaafa-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aaafa-142">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="aaafa-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aaafa-143">INPUTOBJECT <IHealthBotIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="aaafa-143">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aaafa-144">`[BotName <String>]`： Bot 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="aaafa-144">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="aaafa-145">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="aaafa-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aaafa-146">`[ResourceGroupName <String>]`：使用者訂閱中 Bot 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="aaafa-146">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="aaafa-147">`[SubscriptionId <String>]`： Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="aaafa-147">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="aaafa-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="aaafa-148">RELATED LINKS</span></span>


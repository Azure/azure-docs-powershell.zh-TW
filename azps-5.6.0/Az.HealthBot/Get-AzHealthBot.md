---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/get-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
ms.openlocfilehash: 1e9360c7545b1a8c566e1a373b8650e6b6800323
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917230"
---
# <span data-ttu-id="f2aea-101">Get-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="f2aea-101">Get-AzHealthBot</span></span>

## <span data-ttu-id="f2aea-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f2aea-102">SYNOPSIS</span></span>
<span data-ttu-id="f2aea-103">取得 HealthBot。</span><span class="sxs-lookup"><span data-stu-id="f2aea-103">Get a HealthBot.</span></span>

## <span data-ttu-id="f2aea-104">語法</span><span class="sxs-lookup"><span data-stu-id="f2aea-104">SYNTAX</span></span>

### <span data-ttu-id="f2aea-105">清單1 (預設) </span><span class="sxs-lookup"><span data-stu-id="f2aea-105">List1 (Default)</span></span>
```
Get-AzHealthBot [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f2aea-106">獲取</span><span class="sxs-lookup"><span data-stu-id="f2aea-106">Get</span></span>
```
Get-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f2aea-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f2aea-107">GetViaIdentity</span></span>
```
Get-AzHealthBot -InputObject <IHealthBotIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f2aea-108">清單</span><span class="sxs-lookup"><span data-stu-id="f2aea-108">List</span></span>
```
Get-AzHealthBot -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2aea-109">描述</span><span class="sxs-lookup"><span data-stu-id="f2aea-109">DESCRIPTION</span></span>
<span data-ttu-id="f2aea-110">取得 HealthBot。</span><span class="sxs-lookup"><span data-stu-id="f2aea-110">Get a HealthBot.</span></span>

## <span data-ttu-id="f2aea-111">例子</span><span class="sxs-lookup"><span data-stu-id="f2aea-111">EXAMPLES</span></span>

### <span data-ttu-id="f2aea-112">範例 1：取得 All HealthBot</span><span class="sxs-lookup"><span data-stu-id="f2aea-112">Example 1: Get all HealthBot</span></span>
```powershell
PS C:\> Get-AzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="f2aea-113">取得所有 HealthBot</span><span class="sxs-lookup"><span data-stu-id="f2aea-113">Get all HealthBot</span></span>

### <span data-ttu-id="f2aea-114">範例 2：取得 ResourceGroupName 的所有 HealthBot</span><span class="sxs-lookup"><span data-stu-id="f2aea-114">Example 2: Get all HealthBot by ResourceGroupName</span></span>
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="f2aea-115">使用 ResourceGroupName 取得所有 HealthBot</span><span class="sxs-lookup"><span data-stu-id="f2aea-115">Get all HealthBot by ResourceGroupName</span></span>

### <span data-ttu-id="f2aea-116">範例 3：取得 HealthBot by ResourceGroupName 和 Name</span><span class="sxs-lookup"><span data-stu-id="f2aea-116">Example 3: Get HealthBot by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="f2aea-117">按 ResourceGroupName 和 Name 取得 HealthBot</span><span class="sxs-lookup"><span data-stu-id="f2aea-117">Get HealthBot by ResourceGroupName and Name</span></span>

### <span data-ttu-id="f2aea-118">範例 4：Get HealthBot by InputObject</span><span class="sxs-lookup"><span data-stu-id="f2aea-118">Example 4: Get HealthBot by InputObject</span></span>
```powershell
PS C:\> $getAzHealthBot = Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot
Get-AzHealthBot -InputObject $getAzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="f2aea-119">使用 InputObject 取得 HealthBot</span><span class="sxs-lookup"><span data-stu-id="f2aea-119">Get HealthBot by InputObject</span></span>

## <span data-ttu-id="f2aea-120">參數</span><span class="sxs-lookup"><span data-stu-id="f2aea-120">PARAMETERS</span></span>

### <span data-ttu-id="f2aea-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2aea-121">-DefaultProfile</span></span>
<span data-ttu-id="f2aea-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2aea-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2aea-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2aea-123">-InputObject</span></span>
<span data-ttu-id="f2aea-124">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f2aea-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f2aea-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="f2aea-125">-Name</span></span>
<span data-ttu-id="f2aea-126">Bot 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2aea-126">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="f2aea-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2aea-127">-ResourceGroupName</span></span>
<span data-ttu-id="f2aea-128">使用者訂閱中的 Bot 資源組名。</span><span class="sxs-lookup"><span data-stu-id="f2aea-128">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="f2aea-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f2aea-129">-SubscriptionId</span></span>
<span data-ttu-id="f2aea-130">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="f2aea-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="f2aea-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2aea-131">CommonParameters</span></span>
<span data-ttu-id="f2aea-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f2aea-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2aea-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2aea-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2aea-134">輸入</span><span class="sxs-lookup"><span data-stu-id="f2aea-134">INPUTS</span></span>

### <span data-ttu-id="f2aea-135">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="f2aea-135">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="f2aea-136">輸出</span><span class="sxs-lookup"><span data-stu-id="f2aea-136">OUTPUTS</span></span>

### <span data-ttu-id="f2aea-137">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="f2aea-137">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="f2aea-138">筆記</span><span class="sxs-lookup"><span data-stu-id="f2aea-138">NOTES</span></span>

<span data-ttu-id="f2aea-139">別名</span><span class="sxs-lookup"><span data-stu-id="f2aea-139">ALIASES</span></span>

<span data-ttu-id="f2aea-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="f2aea-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f2aea-141">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f2aea-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f2aea-142">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="f2aea-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f2aea-143">INPUTOBJECT： <IHealthBotIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="f2aea-143">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f2aea-144">`[BotName <String>]`：Bot 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2aea-144">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="f2aea-145">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="f2aea-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f2aea-146">`[ResourceGroupName <String>]`：使用者訂閱中的 Bot 資源組名。</span><span class="sxs-lookup"><span data-stu-id="f2aea-146">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="f2aea-147">`[SubscriptionId <String>]`：Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="f2aea-147">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="f2aea-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2aea-148">RELATED LINKS</span></span>


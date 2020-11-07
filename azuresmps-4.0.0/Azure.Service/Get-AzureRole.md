---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C50472E-CE36-4BF1-92C9-A3B9B183ACD1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 929b439c58c344a1902c497bbad6e056e3755025
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967760"
---
# <span data-ttu-id="006e5-101">Get-AzureRole</span><span class="sxs-lookup"><span data-stu-id="006e5-101">Get-AzureRole</span></span>

## <span data-ttu-id="006e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="006e5-102">SYNOPSIS</span></span>
<span data-ttu-id="006e5-103">在您的 Microsoft Azure 服務中傳回角色清單。</span><span class="sxs-lookup"><span data-stu-id="006e5-103">Returns a list of roles in your Microsoft Azure service.</span></span>

## <span data-ttu-id="006e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="006e5-104">SYNTAX</span></span>

```
Get-AzureRole [-ServiceName] <String> [[-Slot] <String>] [[-RoleName] <String>] [-InstanceDetails]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="006e5-105">說明</span><span class="sxs-lookup"><span data-stu-id="006e5-105">DESCRIPTION</span></span>
<span data-ttu-id="006e5-106">**AzureRole** Cmdlet 會傳回清單物件，其中包含 Microsoft Azure 服務中角色的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="006e5-106">The **Get-AzureRole** cmdlet returns a list object with details on the roles in your Microsoft Azure service.</span></span>
<span data-ttu-id="006e5-107">如果您指定角色 **AzureRole** *參數，* 只會傳回該角色的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="006e5-107">If you specify the *RoleName* parameter, **Get-AzureRole** returns details on that role only.</span></span>
<span data-ttu-id="006e5-108">如果您指定 *InstanceDetails* 參數，則會傳回額外的實例特定詳細資料。</span><span class="sxs-lookup"><span data-stu-id="006e5-108">If you specify the *InstanceDetails* parameter, additional, instance-specific details are returned.</span></span>

## <span data-ttu-id="006e5-109">示例</span><span class="sxs-lookup"><span data-stu-id="006e5-109">EXAMPLES</span></span>

### <span data-ttu-id="006e5-110">範例1：取得服務角色的清單</span><span class="sxs-lookup"><span data-stu-id="006e5-110">Example 1: Get a list of roles for a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production"
```

<span data-ttu-id="006e5-111">這個命令會傳回一個物件，其中包含在 MySvc01 服務上執行的所有生產角色的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="006e5-111">This command returns an object with details on all the production roles running on the MySvc01 service.</span></span>

### <span data-ttu-id="006e5-112">範例2：取得服務上執行之角色的詳細資料</span><span class="sxs-lookup"><span data-stu-id="006e5-112">Example 2: Get details on a role running on a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc1" -Slot "Staging" -RoleName "MyTestVM3"
```

<span data-ttu-id="006e5-113">這個命令會傳回一個物件，其中包含 MyTestVM3 角色的詳細資料，在 MySvc01 服務的暫存環境中執行。</span><span class="sxs-lookup"><span data-stu-id="006e5-113">This command returns an object with details on the MyTestVM3 role, running on the staging environment of the MySvc01 service.</span></span>

### <span data-ttu-id="006e5-114">範例3：取得服務上執行的角色實例資訊</span><span class="sxs-lookup"><span data-stu-id="006e5-114">Example 3: Get instance information on instances of a role running on a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -RoleName "MyTestVM02" -InstanceDetails
```

<span data-ttu-id="006e5-115">這個命令會傳回一個物件，其中包含在 MySvc01 服務的生產環境中執行之 MyTestVM02 角色之實例的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="006e5-115">This command returns an object with details on the instances of the MyTestVM02 role running in the production environment on the MySvc01 service.</span></span>

### <span data-ttu-id="006e5-116">範例4：取得與服務相關聯之角色實例的表格</span><span class="sxs-lookup"><span data-stu-id="006e5-116">Example 4: Get a table of the role instances associated with a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -InstanceDetails | Format-Table -Auto "InstanceName", "InstanceSize", "InstanceStatus"
```

<span data-ttu-id="006e5-117">這個命令會傳回在 MySvc01 服務的生產環境中執行的所有角色實例之實例名稱、大小及狀態的表格。</span><span class="sxs-lookup"><span data-stu-id="006e5-117">This command returns a table of the instance name, size, and status of all role instances running in the production environment on the MySvc01 service.</span></span>

## <span data-ttu-id="006e5-118">參數</span><span class="sxs-lookup"><span data-stu-id="006e5-118">PARAMETERS</span></span>

### <span data-ttu-id="006e5-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="006e5-119">-InformationAction</span></span>
<span data-ttu-id="006e5-120">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="006e5-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="006e5-121">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="006e5-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="006e5-122">持續</span><span class="sxs-lookup"><span data-stu-id="006e5-122">Continue</span></span>
- <span data-ttu-id="006e5-123">理會</span><span class="sxs-lookup"><span data-stu-id="006e5-123">Ignore</span></span>
- <span data-ttu-id="006e5-124">看</span><span class="sxs-lookup"><span data-stu-id="006e5-124">Inquire</span></span>
- <span data-ttu-id="006e5-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="006e5-125">SilentlyContinue</span></span>
- <span data-ttu-id="006e5-126">停止</span><span class="sxs-lookup"><span data-stu-id="006e5-126">Stop</span></span>
- <span data-ttu-id="006e5-127">封存</span><span class="sxs-lookup"><span data-stu-id="006e5-127">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="006e5-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="006e5-128">-InformationVariable</span></span>
<span data-ttu-id="006e5-129">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="006e5-129">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="006e5-130">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="006e5-130">-InstanceDetails</span></span>
<span data-ttu-id="006e5-131">指定此 Cmdlet 會傳回有關每個角色上之實例的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="006e5-131">Specifies that this cmdlet returns details about the instances on each role.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="006e5-132">-設定檔</span><span class="sxs-lookup"><span data-stu-id="006e5-132">-Profile</span></span>
<span data-ttu-id="006e5-133">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="006e5-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="006e5-134">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="006e5-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="006e5-135">-擁有方</span><span class="sxs-lookup"><span data-stu-id="006e5-135">-RoleName</span></span>
<span data-ttu-id="006e5-136">指定要取得的角色名稱。</span><span class="sxs-lookup"><span data-stu-id="006e5-136">Specifies the name of the role to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="006e5-137">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="006e5-137">-ServiceName</span></span>
<span data-ttu-id="006e5-138">指定 Azure 服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="006e5-138">Specifies the name of the Azure service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="006e5-139">-槽</span><span class="sxs-lookup"><span data-stu-id="006e5-139">-Slot</span></span>
<span data-ttu-id="006e5-140">指定 Azure 部署環境。</span><span class="sxs-lookup"><span data-stu-id="006e5-140">Specifies the Azure deployment environment.</span></span>
<span data-ttu-id="006e5-141">此參數可接受的值為： [生產] 或 [轉移]。</span><span class="sxs-lookup"><span data-stu-id="006e5-141">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="006e5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="006e5-142">CommonParameters</span></span>
<span data-ttu-id="006e5-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="006e5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="006e5-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="006e5-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="006e5-145">輸入</span><span class="sxs-lookup"><span data-stu-id="006e5-145">INPUTS</span></span>

## <span data-ttu-id="006e5-146">輸出</span><span class="sxs-lookup"><span data-stu-id="006e5-146">OUTPUTS</span></span>

## <span data-ttu-id="006e5-147">筆記</span><span class="sxs-lookup"><span data-stu-id="006e5-147">NOTES</span></span>

## <span data-ttu-id="006e5-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="006e5-148">RELATED LINKS</span></span>

[<span data-ttu-id="006e5-149">Set-AzureRole</span><span class="sxs-lookup"><span data-stu-id="006e5-149">Set-AzureRole</span></span>](./Set-AzureRole.md)



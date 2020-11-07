---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2AEA385F-E180-4564-A62A-9E913C665801
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fff3ea97c51ee5597e585f3275b25e513c22008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966926"
---
# <span data-ttu-id="de9ab-101">Reset-AzureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="de9ab-101">Reset-AzureRoleInstance</span></span>

## <span data-ttu-id="de9ab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="de9ab-102">SYNOPSIS</span></span>
<span data-ttu-id="de9ab-103">要求單一角色實例的重新開機或重新鏡像，或特定角色的所有角色實例。</span><span class="sxs-lookup"><span data-stu-id="de9ab-103">Requests a reboot or reimage of a single role instance or all role instances of a specific role.</span></span>

## <span data-ttu-id="de9ab-104">句法</span><span class="sxs-lookup"><span data-stu-id="de9ab-104">SYNTAX</span></span>

```
Reset-AzureRoleInstance [-ServiceName] <String> -Slot <String> -InstanceName <String> [-Reboot] [-Reimage]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="de9ab-105">說明</span><span class="sxs-lookup"><span data-stu-id="de9ab-105">DESCRIPTION</span></span>
<span data-ttu-id="de9ab-106">**Reset AzureRoleInstance** Cmdlet 會要求重新開機或重新鏡像在部署中執行的角色實例。</span><span class="sxs-lookup"><span data-stu-id="de9ab-106">The **Reset-AzureRoleInstance** cmdlet requests a reboot or a reimage of a role instance that is running in a deployment.</span></span>
<span data-ttu-id="de9ab-107">此操作會同步執行。</span><span class="sxs-lookup"><span data-stu-id="de9ab-107">This operation executes synchronously.</span></span>
<span data-ttu-id="de9ab-108">當您重新開機角色實例時，Azure 會將實例設為離線，重新開機該實例的基礎作業系統，然後將該實例傳回線上。</span><span class="sxs-lookup"><span data-stu-id="de9ab-108">When you reboot a role instance, Azure takes the instance offline, restarts the underlying operating system for that instance, and brings the instance back online.</span></span>
<span data-ttu-id="de9ab-109">任何寫入本機磁片的資料都會在重新開機後繼續。</span><span class="sxs-lookup"><span data-stu-id="de9ab-109">Any data that is written to the local disk persists across reboots.</span></span>
<span data-ttu-id="de9ab-110">任何記憶體中的資料都會遺失。</span><span class="sxs-lookup"><span data-stu-id="de9ab-110">Any data that is in-memory is lost.</span></span>

<span data-ttu-id="de9ab-111">根據角色類型，對角色實例進行映射，會產生不同的行為。</span><span class="sxs-lookup"><span data-stu-id="de9ab-111">Reimaging a role instance results in different behavior depending on the type of role.</span></span>
<span data-ttu-id="de9ab-112">針對網站或 worker 角色，當角色為 reimaged 時，Azure 會將該角色設為離線，並將 Azure 客體作業系統的全新安裝寫入虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="de9ab-112">For a web or worker role, when the role is reimaged, Azure takes the role offline and writes a fresh installation of the Azure guest operating system to the virtual machine.</span></span>
<span data-ttu-id="de9ab-113">然後，角色就會再次回到線上。</span><span class="sxs-lookup"><span data-stu-id="de9ab-113">The role is then brought back online.</span></span>
<span data-ttu-id="de9ab-114">針對 VM 角色，當角色為 reimaged 時，Azure 會將角色設為離線，重新應用您提供給它的自訂影像，然後使角色回到線上。</span><span class="sxs-lookup"><span data-stu-id="de9ab-114">For a VM role, when the role is reimaged, Azure takes the role offline, reapplies the custom image that you provided for it, and brings the role back online.</span></span>

<span data-ttu-id="de9ab-115">當角色為 reimaged 時，Azure 會嘗試在任何本機存儲資源中維護資料;不過，如果暫時性的硬體失敗，本機儲存資源可能會遺失。</span><span class="sxs-lookup"><span data-stu-id="de9ab-115">Azure attempts to maintain data in any local storage resources when the role is reimaged; however, in case of a transient hardware failure, the local storage resource may be lost.</span></span>
<span data-ttu-id="de9ab-116">如果您的應用程式要求資料保持不變，建議寫入持久資料來源（例如 Azure 磁碟機）。</span><span class="sxs-lookup"><span data-stu-id="de9ab-116">If your application requires that data persist, writing to a durable data source, such as an Azure drive, is recommended.</span></span>
<span data-ttu-id="de9ab-117">如果角色是 reimaged，則任何寫入本機存儲資源所定義的本地目錄以外的資料都會遺失。</span><span class="sxs-lookup"><span data-stu-id="de9ab-117">Any data that is written to a local directory other than that defined by the local storage resource will be lost when the role is reimaged.</span></span>

## <span data-ttu-id="de9ab-118">示例</span><span class="sxs-lookup"><span data-stu-id="de9ab-118">EXAMPLES</span></span>

### <span data-ttu-id="de9ab-119">範例1：重新開機角色實例</span><span class="sxs-lookup"><span data-stu-id="de9ab-119">Example 1: Reboot a role instance</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -InstanceName "MyWebRole_IN_0" -Reboot
```

<span data-ttu-id="de9ab-120">這個命令會在 MySvc01 服務的暫存部署中重新開機名為 MyWebRole_IN_0 的角色實例。</span><span class="sxs-lookup"><span data-stu-id="de9ab-120">This command reboots the role instance named MyWebRole_IN_0 in the staging deployment of the MySvc01 service.</span></span>

### <span data-ttu-id="de9ab-121">範例2：重新鏡像角色實例</span><span class="sxs-lookup"><span data-stu-id="de9ab-121">Example 2: Reimage a role instance</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -Reimage
```

<span data-ttu-id="de9ab-122">這個命令會 reimages MySvc01 雲端服務的過渡部署中的角色實例。</span><span class="sxs-lookup"><span data-stu-id="de9ab-122">This command reimages the role instances in the staging deployment of the MySvc01 cloud service.</span></span>

### <span data-ttu-id="de9ab-123">範例3：重新鏡像所有角色實例</span><span class="sxs-lookup"><span data-stu-id="de9ab-123">Example 3: Reimage all role instances</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc1" -Slot "Production" -Reimage
```

<span data-ttu-id="de9ab-124">此命令會 reimages MySvc01 服務的生產部署中的所有角色實例。</span><span class="sxs-lookup"><span data-stu-id="de9ab-124">This command reimages all role instances in the production deployment of the MySvc01 service.</span></span>

## <span data-ttu-id="de9ab-125">參數</span><span class="sxs-lookup"><span data-stu-id="de9ab-125">PARAMETERS</span></span>

### <span data-ttu-id="de9ab-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="de9ab-126">-InformationAction</span></span>
<span data-ttu-id="de9ab-127">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="de9ab-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="de9ab-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="de9ab-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="de9ab-129">持續</span><span class="sxs-lookup"><span data-stu-id="de9ab-129">Continue</span></span>
- <span data-ttu-id="de9ab-130">理會</span><span class="sxs-lookup"><span data-stu-id="de9ab-130">Ignore</span></span>
- <span data-ttu-id="de9ab-131">看</span><span class="sxs-lookup"><span data-stu-id="de9ab-131">Inquire</span></span>
- <span data-ttu-id="de9ab-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="de9ab-132">SilentlyContinue</span></span>
- <span data-ttu-id="de9ab-133">停止</span><span class="sxs-lookup"><span data-stu-id="de9ab-133">Stop</span></span>
- <span data-ttu-id="de9ab-134">封存</span><span class="sxs-lookup"><span data-stu-id="de9ab-134">Suspend</span></span>

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

### <span data-ttu-id="de9ab-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="de9ab-135">-InformationVariable</span></span>
<span data-ttu-id="de9ab-136">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="de9ab-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="de9ab-137">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="de9ab-137">-InstanceName</span></span>
<span data-ttu-id="de9ab-138">指定要重新映射或重新開機的角色實例名稱。</span><span class="sxs-lookup"><span data-stu-id="de9ab-138">Specifies the name of the role instance to reimage or reboot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de9ab-139">-設定檔</span><span class="sxs-lookup"><span data-stu-id="de9ab-139">-Profile</span></span>
<span data-ttu-id="de9ab-140">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="de9ab-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="de9ab-141">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="de9ab-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="de9ab-142">-重新開機</span><span class="sxs-lookup"><span data-stu-id="de9ab-142">-Reboot</span></span>
<span data-ttu-id="de9ab-143">指定此 Cmdlet 會重新開機指定的角色實例，或者如果沒有指定，則是所有角色實例。</span><span class="sxs-lookup"><span data-stu-id="de9ab-143">Specifies that this cmdlet reboots the specified role instance or, if none is specified, all role instances.</span></span>
<span data-ttu-id="de9ab-144">您必須包含 *重新開機* 或重新 *映射* 參數，但不能同時包含兩者。</span><span class="sxs-lookup"><span data-stu-id="de9ab-144">You must include either a *Reboot* or *Reimage* parameter, but not both.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de9ab-145">-重新映射</span><span class="sxs-lookup"><span data-stu-id="de9ab-145">-Reimage</span></span>
<span data-ttu-id="de9ab-146">指定此 Cmdlet 會 reimages 指定的角色實例，或者如果沒有指定，則是所有角色實例。</span><span class="sxs-lookup"><span data-stu-id="de9ab-146">Specifies that this cmdlet reimages the specified role instance or, if none is specified, all role instances.</span></span>
<span data-ttu-id="de9ab-147">您必須包含 *重新開機* 或重新 *映射* 參數，但不能同時包含兩者。</span><span class="sxs-lookup"><span data-stu-id="de9ab-147">You must include either a *Reboot* or *Reimage* parameter, but not both.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de9ab-148">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="de9ab-148">-ServiceName</span></span>
<span data-ttu-id="de9ab-149">指定服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="de9ab-149">Specifies the name of the service.</span></span>

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

### <span data-ttu-id="de9ab-150">-槽</span><span class="sxs-lookup"><span data-stu-id="de9ab-150">-Slot</span></span>
<span data-ttu-id="de9ab-151">指定角色實例執行所在的部署環境。</span><span class="sxs-lookup"><span data-stu-id="de9ab-151">Specifies the deployment environment where the role instances run.</span></span>
<span data-ttu-id="de9ab-152">有效值為： [生產] 和 [轉移]。</span><span class="sxs-lookup"><span data-stu-id="de9ab-152">Valid values are: Production and Staging.</span></span>
<span data-ttu-id="de9ab-153">您可以包含 *DeploymentName* 或 *槽* 參數，但不能同時包含兩者。</span><span class="sxs-lookup"><span data-stu-id="de9ab-153">You can include either the *DeploymentName* or *Slot* parameter, but not both.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de9ab-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de9ab-154">CommonParameters</span></span>
<span data-ttu-id="de9ab-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="de9ab-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de9ab-156">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="de9ab-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de9ab-157">輸入</span><span class="sxs-lookup"><span data-stu-id="de9ab-157">INPUTS</span></span>

## <span data-ttu-id="de9ab-158">輸出</span><span class="sxs-lookup"><span data-stu-id="de9ab-158">OUTPUTS</span></span>

## <span data-ttu-id="de9ab-159">筆記</span><span class="sxs-lookup"><span data-stu-id="de9ab-159">NOTES</span></span>

## <span data-ttu-id="de9ab-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="de9ab-160">RELATED LINKS</span></span>

[<span data-ttu-id="de9ab-161">Set-AzureRole</span><span class="sxs-lookup"><span data-stu-id="de9ab-161">Set-AzureRole</span></span>](./Set-AzureRole.md)



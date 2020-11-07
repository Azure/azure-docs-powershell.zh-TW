---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95298AFC-B492-4EA6-AFC2-E862D3086AF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84b1256d7d911d22a4f1344bdf841943ce87ee7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967562"
---
# <span data-ttu-id="65bd4-101">Remove-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="65bd4-101">Remove-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="65bd4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="65bd4-102">SYNOPSIS</span></span>
<span data-ttu-id="65bd4-103">移除在特定部署槽中針對所有角色或命名角色所套用的雲端服務診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="65bd4-103">Removes the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="65bd4-104">句法</span><span class="sxs-lookup"><span data-stu-id="65bd4-104">SYNTAX</span></span>

### <span data-ttu-id="65bd4-105">RemoveByRoles (預設) </span><span class="sxs-lookup"><span data-stu-id="65bd4-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="65bd4-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="65bd4-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [-UninstallConfiguration]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="65bd4-107">說明</span><span class="sxs-lookup"><span data-stu-id="65bd4-107">DESCRIPTION</span></span>
<span data-ttu-id="65bd4-108">**AzureServiceDiagnosticsExtension** Cmdlet 會移除在特定部署槽中針對所有角色或命名角色所套用的雲端服務診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="65bd4-108">The **Remove-AzureServiceDiagnosticsExtension** cmdlet removes the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="65bd4-109">示例</span><span class="sxs-lookup"><span data-stu-id="65bd4-109">EXAMPLES</span></span>

### <span data-ttu-id="65bd4-110">範例1：移除服務的診斷延伸</span><span class="sxs-lookup"><span data-stu-id="65bd4-110">Example 1: Remove the diagnostic extension for a service</span></span>
```
PS C:\> Remove-AzureServiceDiagnosticsExtension -ServiceName $Svc
```

<span data-ttu-id="65bd4-111">這個命令會移除指定角色的診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="65bd4-111">This command removes the diagnostic extension for a specified role.</span></span>

### <span data-ttu-id="65bd4-112">範例2：移除指定角色中服務的診斷延伸</span><span class="sxs-lookup"><span data-stu-id="65bd4-112">Example 2: Remove the diagnostic extension for a service in a specified role</span></span>
```
PS C:\> Remove-AzureServiceDiagnosticsExtension -ServiceName $Svc -Role "WebRole01"
```

<span data-ttu-id="65bd4-113">這個命令會移除指定角色的診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="65bd4-113">This command removes the diagnostic extension for a specified role.</span></span>

## <span data-ttu-id="65bd4-114">參數</span><span class="sxs-lookup"><span data-stu-id="65bd4-114">PARAMETERS</span></span>

### <span data-ttu-id="65bd4-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="65bd4-115">-InformationAction</span></span>
<span data-ttu-id="65bd4-116">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="65bd4-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="65bd4-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="65bd4-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="65bd4-118">持續</span><span class="sxs-lookup"><span data-stu-id="65bd4-118">Continue</span></span>
- <span data-ttu-id="65bd4-119">理會</span><span class="sxs-lookup"><span data-stu-id="65bd4-119">Ignore</span></span>
- <span data-ttu-id="65bd4-120">看</span><span class="sxs-lookup"><span data-stu-id="65bd4-120">Inquire</span></span>
- <span data-ttu-id="65bd4-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="65bd4-121">SilentlyContinue</span></span>
- <span data-ttu-id="65bd4-122">停止</span><span class="sxs-lookup"><span data-stu-id="65bd4-122">Stop</span></span>
- <span data-ttu-id="65bd4-123">封存</span><span class="sxs-lookup"><span data-stu-id="65bd4-123">Suspend</span></span>

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

### <span data-ttu-id="65bd4-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="65bd4-124">-InformationVariable</span></span>
<span data-ttu-id="65bd4-125">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="65bd4-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="65bd4-126">-設定檔</span><span class="sxs-lookup"><span data-stu-id="65bd4-126">-Profile</span></span>
<span data-ttu-id="65bd4-127">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="65bd4-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="65bd4-128">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="65bd4-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="65bd4-129">-角色</span><span class="sxs-lookup"><span data-stu-id="65bd4-129">-Role</span></span>
<span data-ttu-id="65bd4-130">指定要指定其遠端桌面設定的選擇性角色陣列。</span><span class="sxs-lookup"><span data-stu-id="65bd4-130">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="65bd4-131">如果您沒有指定此參數，則會將遠端桌面設定套用為所有角色的預設配置。</span><span class="sxs-lookup"><span data-stu-id="65bd4-131">If you do not specify this parameter, the remote desktop configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: RemoveByRoles
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65bd4-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="65bd4-132">-ServiceName</span></span>
<span data-ttu-id="65bd4-133">指定部署的 Azure 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="65bd4-133">Specifies the Azure service name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65bd4-134">-槽</span><span class="sxs-lookup"><span data-stu-id="65bd4-134">-Slot</span></span>
<span data-ttu-id="65bd4-135">指定要修改的部署環境。</span><span class="sxs-lookup"><span data-stu-id="65bd4-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="65bd4-136">有效值為 [生產] 或 [轉移]。</span><span class="sxs-lookup"><span data-stu-id="65bd4-136">Valid values are Production or Staging.</span></span>

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

### <span data-ttu-id="65bd4-137">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="65bd4-137">-UninstallConfiguration</span></span>
<span data-ttu-id="65bd4-138">表示此 Cmdlet 會從雲端服務卸載所有 RDP 設定。</span><span class="sxs-lookup"><span data-stu-id="65bd4-138">Indicates that this cmdlet uninstalls all RDP configurations from the cloud service.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAllRoles
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65bd4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65bd4-139">CommonParameters</span></span>
<span data-ttu-id="65bd4-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="65bd4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65bd4-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="65bd4-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65bd4-142">輸入</span><span class="sxs-lookup"><span data-stu-id="65bd4-142">INPUTS</span></span>

## <span data-ttu-id="65bd4-143">輸出</span><span class="sxs-lookup"><span data-stu-id="65bd4-143">OUTPUTS</span></span>

## <span data-ttu-id="65bd4-144">筆記</span><span class="sxs-lookup"><span data-stu-id="65bd4-144">NOTES</span></span>

## <span data-ttu-id="65bd4-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="65bd4-145">RELATED LINKS</span></span>

[<span data-ttu-id="65bd4-146">AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="65bd4-146">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="65bd4-147">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="65bd4-147">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)



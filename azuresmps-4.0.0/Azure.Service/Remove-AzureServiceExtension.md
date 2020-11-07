---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6B5E4968-5DF5-4956-A070-9F54A79D960B
online version: ''
schema: 2.0.0
ms.openlocfilehash: f45e0a93b2f6261ca6031aa721bda3a72f4443dd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967559"
---
# <span data-ttu-id="6c4e6-101">Remove-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="6c4e6-101">Remove-AzureServiceExtension</span></span>

## <span data-ttu-id="6c4e6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6c4e6-102">SYNOPSIS</span></span>
<span data-ttu-id="6c4e6-103">移除在部署中套用的雲端服務延伸。</span><span class="sxs-lookup"><span data-stu-id="6c4e6-103">Removes cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="6c4e6-104">句法</span><span class="sxs-lookup"><span data-stu-id="6c4e6-104">SYNTAX</span></span>

### <span data-ttu-id="6c4e6-105">RemoveByRoles (預設) </span><span class="sxs-lookup"><span data-stu-id="6c4e6-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-ExtensionName] <String> [-ProviderNamespace] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6c4e6-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="6c4e6-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-UninstallConfiguration] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6c4e6-107">說明</span><span class="sxs-lookup"><span data-stu-id="6c4e6-107">DESCRIPTION</span></span>
<span data-ttu-id="6c4e6-108">**AzureServiceExtension** Cmdlet 會移除在部署中套用的雲端服務擴展。</span><span class="sxs-lookup"><span data-stu-id="6c4e6-108">The **Remove-AzureServiceExtension** cmdlet removes cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="6c4e6-109">示例</span><span class="sxs-lookup"><span data-stu-id="6c4e6-109">EXAMPLES</span></span>

### <span data-ttu-id="6c4e6-110">範例1：移除服務延伸</span><span class="sxs-lookup"><span data-stu-id="6c4e6-110">Example 1: Remove a service extension</span></span>
```
PS C:\> Remove-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions"
```

<span data-ttu-id="6c4e6-111">這個命令會移除服務延伸。</span><span class="sxs-lookup"><span data-stu-id="6c4e6-111">This command removes a service extension.</span></span>

### <span data-ttu-id="6c4e6-112">範例2：移除服務延伸並卸載所有設定</span><span class="sxs-lookup"><span data-stu-id="6c4e6-112">Example 2: Remove a service extension and uninstall all configurations</span></span>
```
PS C:\> Remove-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -UninstallConfiguration
```

<span data-ttu-id="6c4e6-113">這個命令會移除服務延伸並卸載所有設定。</span><span class="sxs-lookup"><span data-stu-id="6c4e6-113">This command removes a service extension and uninstalls all configurations.</span></span>

## <span data-ttu-id="6c4e6-114">參數</span><span class="sxs-lookup"><span data-stu-id="6c4e6-114">PARAMETERS</span></span>

### <span data-ttu-id="6c4e6-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="6c4e6-115">-ExtensionName</span></span>
<span data-ttu-id="6c4e6-116">指定副檔名。</span><span class="sxs-lookup"><span data-stu-id="6c4e6-116">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c4e6-117">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6c4e6-117">-InformationAction</span></span>
<span data-ttu-id="6c4e6-118">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="6c4e6-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6c4e6-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6c4e6-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6c4e6-120">持續</span><span class="sxs-lookup"><span data-stu-id="6c4e6-120">Continue</span></span>
- <span data-ttu-id="6c4e6-121">理會</span><span class="sxs-lookup"><span data-stu-id="6c4e6-121">Ignore</span></span>
- <span data-ttu-id="6c4e6-122">看</span><span class="sxs-lookup"><span data-stu-id="6c4e6-122">Inquire</span></span>
- <span data-ttu-id="6c4e6-123">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6c4e6-123">SilentlyContinue</span></span>
- <span data-ttu-id="6c4e6-124">停止</span><span class="sxs-lookup"><span data-stu-id="6c4e6-124">Stop</span></span>
- <span data-ttu-id="6c4e6-125">封存</span><span class="sxs-lookup"><span data-stu-id="6c4e6-125">Suspend</span></span>

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

### <span data-ttu-id="6c4e6-126">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6c4e6-126">-InformationVariable</span></span>
<span data-ttu-id="6c4e6-127">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="6c4e6-127">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6c4e6-128">-設定檔</span><span class="sxs-lookup"><span data-stu-id="6c4e6-128">-Profile</span></span>
<span data-ttu-id="6c4e6-129">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="6c4e6-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6c4e6-130">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="6c4e6-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6c4e6-131">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="6c4e6-131">-ProviderNamespace</span></span>
<span data-ttu-id="6c4e6-132">指定延伸提供者命名空間。</span><span class="sxs-lookup"><span data-stu-id="6c4e6-132">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c4e6-133">-角色</span><span class="sxs-lookup"><span data-stu-id="6c4e6-133">-Role</span></span>
<span data-ttu-id="6c4e6-134">指定要為其指定副檔名的選擇性角色陣列。</span><span class="sxs-lookup"><span data-stu-id="6c4e6-134">Specifies an optional array of roles to specify the extension for.</span></span>
<span data-ttu-id="6c4e6-135">如果未指定，延伸會套用為所有角色的預設配置。</span><span class="sxs-lookup"><span data-stu-id="6c4e6-135">If not specified the extension is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="6c4e6-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6c4e6-136">-ServiceName</span></span>
<span data-ttu-id="6c4e6-137">指定雲端服務名稱。</span><span class="sxs-lookup"><span data-stu-id="6c4e6-137">Specifies the cloud service name.</span></span>

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

### <span data-ttu-id="6c4e6-138">-槽</span><span class="sxs-lookup"><span data-stu-id="6c4e6-138">-Slot</span></span>
<span data-ttu-id="6c4e6-139">指定要修改的部署環境。</span><span class="sxs-lookup"><span data-stu-id="6c4e6-139">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="6c4e6-140">有效值為 [生產] 或 [轉移]。</span><span class="sxs-lookup"><span data-stu-id="6c4e6-140">Valid values are Production or Staging.</span></span>

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

### <span data-ttu-id="6c4e6-141">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c4e6-141">-UninstallConfiguration</span></span>
<span data-ttu-id="6c4e6-142">表示此 Cmdlet 會從雲端服務卸載所有配置。</span><span class="sxs-lookup"><span data-stu-id="6c4e6-142">Indicates that this cmdlet uninstalls all configurations from the cloud service.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAllRoles
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c4e6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c4e6-143">CommonParameters</span></span>
<span data-ttu-id="6c4e6-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6c4e6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c4e6-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6c4e6-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c4e6-146">輸入</span><span class="sxs-lookup"><span data-stu-id="6c4e6-146">INPUTS</span></span>

## <span data-ttu-id="6c4e6-147">輸出</span><span class="sxs-lookup"><span data-stu-id="6c4e6-147">OUTPUTS</span></span>

## <span data-ttu-id="6c4e6-148">筆記</span><span class="sxs-lookup"><span data-stu-id="6c4e6-148">NOTES</span></span>

## <span data-ttu-id="6c4e6-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c4e6-149">RELATED LINKS</span></span>

[<span data-ttu-id="6c4e6-150">AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="6c4e6-150">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="6c4e6-151">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="6c4e6-151">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)



---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C263CCAD-E51F-420E-9AD4-4FAC09C99CB1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3c10a7694034fe4400ed415891e74f7089ce8558
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967558"
---
# <span data-ttu-id="81a76-101">Remove-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="81a76-101">Remove-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="81a76-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81a76-102">SYNOPSIS</span></span>
<span data-ttu-id="81a76-103">移除在指定部署槽中針對所有角色或命名角色所套用的雲端服務遠端桌面延伸。</span><span class="sxs-lookup"><span data-stu-id="81a76-103">Removes the cloud service remote desktop extension applied on all roles or named roles at a specified deployment slot.</span></span>

## <span data-ttu-id="81a76-104">句法</span><span class="sxs-lookup"><span data-stu-id="81a76-104">SYNTAX</span></span>

### <span data-ttu-id="81a76-105">RemoveByRoles (預設) </span><span class="sxs-lookup"><span data-stu-id="81a76-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="81a76-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="81a76-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>]
 [-UninstallConfiguration] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="81a76-107">說明</span><span class="sxs-lookup"><span data-stu-id="81a76-107">DESCRIPTION</span></span>
<span data-ttu-id="81a76-108">**AzureServiceRemoteDesktopExtension** Cmdlet 會移除在特定部署槽中針對所有角色或命名角色所套用的雲端服務遠端桌面延伸。</span><span class="sxs-lookup"><span data-stu-id="81a76-108">The **Remove-AzureServiceRemoteDesktopExtension** cmdlet removes the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="81a76-109">示例</span><span class="sxs-lookup"><span data-stu-id="81a76-109">EXAMPLES</span></span>

### <span data-ttu-id="81a76-110">範例1：移除遠端桌面副檔名</span><span class="sxs-lookup"><span data-stu-id="81a76-110">Example 1: Remove the remote desktop extension</span></span>
```
PS C:\> Remove-AzureServiceRemoteDesktopExtension -ServiceName $svc
```

<span data-ttu-id="81a76-111">這個命令會移除遠端桌面延伸。</span><span class="sxs-lookup"><span data-stu-id="81a76-111">This command removes the remote desktop extension.</span></span>

### <span data-ttu-id="81a76-112">範例2：從指定的角色移除遠端桌面延伸</span><span class="sxs-lookup"><span data-stu-id="81a76-112">Example 2: Remove the remote desktop extension from a specified role</span></span>
```
PS C:\> Remove-AzureServiceRemoteDesktopExtension -ServiceName $svc -Role "WebRole1"
```

<span data-ttu-id="81a76-113">這個命令會從指定的角色中移除遠端桌面延伸。</span><span class="sxs-lookup"><span data-stu-id="81a76-113">This command removes the remote desktop extension from a specified role.</span></span>

## <span data-ttu-id="81a76-114">參數</span><span class="sxs-lookup"><span data-stu-id="81a76-114">PARAMETERS</span></span>

### <span data-ttu-id="81a76-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="81a76-115">-InformationAction</span></span>
<span data-ttu-id="81a76-116">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="81a76-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="81a76-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="81a76-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="81a76-118">持續</span><span class="sxs-lookup"><span data-stu-id="81a76-118">Continue</span></span>
- <span data-ttu-id="81a76-119">理會</span><span class="sxs-lookup"><span data-stu-id="81a76-119">Ignore</span></span>
- <span data-ttu-id="81a76-120">看</span><span class="sxs-lookup"><span data-stu-id="81a76-120">Inquire</span></span>
- <span data-ttu-id="81a76-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="81a76-121">SilentlyContinue</span></span>
- <span data-ttu-id="81a76-122">停止</span><span class="sxs-lookup"><span data-stu-id="81a76-122">Stop</span></span>
- <span data-ttu-id="81a76-123">封存</span><span class="sxs-lookup"><span data-stu-id="81a76-123">Suspend</span></span>

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

### <span data-ttu-id="81a76-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="81a76-124">-InformationVariable</span></span>
<span data-ttu-id="81a76-125">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="81a76-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="81a76-126">-設定檔</span><span class="sxs-lookup"><span data-stu-id="81a76-126">-Profile</span></span>
<span data-ttu-id="81a76-127">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="81a76-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="81a76-128">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="81a76-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="81a76-129">-角色</span><span class="sxs-lookup"><span data-stu-id="81a76-129">-Role</span></span>
<span data-ttu-id="81a76-130">指定要為其指定遠端桌面設定的選擇性角色陣列。</span><span class="sxs-lookup"><span data-stu-id="81a76-130">Specifies an optional array of roles to specify the remote desktop configuration for.</span></span>
<span data-ttu-id="81a76-131">如果未指定，遠端桌面設定會套用為所有角色的預設配置。</span><span class="sxs-lookup"><span data-stu-id="81a76-131">If not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="81a76-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="81a76-132">-ServiceName</span></span>
<span data-ttu-id="81a76-133">指定部署的 Azure 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="81a76-133">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="81a76-134">-槽</span><span class="sxs-lookup"><span data-stu-id="81a76-134">-Slot</span></span>
<span data-ttu-id="81a76-135">指定要修改的部署環境。</span><span class="sxs-lookup"><span data-stu-id="81a76-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="81a76-136">支援的值為「生產」或「分段」。</span><span class="sxs-lookup"><span data-stu-id="81a76-136">Supported values are "Production" or "Staging".</span></span>

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

### <span data-ttu-id="81a76-137">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="81a76-137">-UninstallConfiguration</span></span>
<span data-ttu-id="81a76-138">指定此 Cmdlet 會從雲端服務卸載所有 RDP 設定。</span><span class="sxs-lookup"><span data-stu-id="81a76-138">Specifies that this cmdlet uninstalls all RDP configurations from the cloud service.</span></span>

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

### <span data-ttu-id="81a76-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81a76-139">CommonParameters</span></span>
<span data-ttu-id="81a76-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81a76-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81a76-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="81a76-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81a76-142">輸入</span><span class="sxs-lookup"><span data-stu-id="81a76-142">INPUTS</span></span>

## <span data-ttu-id="81a76-143">輸出</span><span class="sxs-lookup"><span data-stu-id="81a76-143">OUTPUTS</span></span>

## <span data-ttu-id="81a76-144">筆記</span><span class="sxs-lookup"><span data-stu-id="81a76-144">NOTES</span></span>

## <span data-ttu-id="81a76-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="81a76-145">RELATED LINKS</span></span>

[<span data-ttu-id="81a76-146">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="81a76-146">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)



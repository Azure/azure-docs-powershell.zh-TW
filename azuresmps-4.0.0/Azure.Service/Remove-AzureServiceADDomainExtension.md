---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6A280C0B-5F55-4575-9B11-596F497C4305
online version: ''
schema: 2.0.0
ms.openlocfilehash: 71e49425724926848ee69b24f5dfca70df664913
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967572"
---
# <span data-ttu-id="c9bf9-101">Remove-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="c9bf9-101">Remove-AzureServiceADDomainExtension</span></span>

## <span data-ttu-id="c9bf9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c9bf9-102">SYNOPSIS</span></span>
<span data-ttu-id="c9bf9-103">移除在特定部署槽中針對所有角色或命名角色所套用的雲端服務 AD 域延伸。</span><span class="sxs-lookup"><span data-stu-id="c9bf9-103">Removes the cloud service AD domain extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="c9bf9-104">句法</span><span class="sxs-lookup"><span data-stu-id="c9bf9-104">SYNTAX</span></span>

### <span data-ttu-id="c9bf9-105">RemoveByRoles (預設) </span><span class="sxs-lookup"><span data-stu-id="c9bf9-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9bf9-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="c9bf9-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [-UninstallConfiguration]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9bf9-107">說明</span><span class="sxs-lookup"><span data-stu-id="c9bf9-107">DESCRIPTION</span></span>
<span data-ttu-id="c9bf9-108">**AzureServiceADDomainExtension** Cmdlet 會移除雲端服務 Active DIRECTORY (AD) 在特定部署槽上套用所有角色或命名角色的網域延伸。</span><span class="sxs-lookup"><span data-stu-id="c9bf9-108">The **Remove-AzureServiceADDomainExtension** cmdlet removes the cloud service Active Directory (AD) domain extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="c9bf9-109">示例</span><span class="sxs-lookup"><span data-stu-id="c9bf9-109">EXAMPLES</span></span>

### <span data-ttu-id="c9bf9-110">範例1：移除 AD 網域延伸</span><span class="sxs-lookup"><span data-stu-id="c9bf9-110">Example 1: Remove an AD domain extension</span></span>
```
PS C:\> Remove-AzureServiceADDomainExtension -ServiceName $Svc
```

<span data-ttu-id="c9bf9-111">這個命令會移除 $Svc 變數所指定的副檔名。</span><span class="sxs-lookup"><span data-stu-id="c9bf9-111">This command removes the extension specified by the $Svc variable.</span></span>

### <span data-ttu-id="c9bf9-112">範例2：移除指定角色的 AD 網域延伸</span><span class="sxs-lookup"><span data-stu-id="c9bf9-112">Example 2: Remove an AD Domain extension for a specified role</span></span>
```
PS C:\> Remove-AzureServiceADDomainExtension -ServiceName $Svc -Role "WebRole1"
```

<span data-ttu-id="c9bf9-113">這個命令會移除指定角色的服務延伸。</span><span class="sxs-lookup"><span data-stu-id="c9bf9-113">This command removes the service extension for the specified role.</span></span>

## <span data-ttu-id="c9bf9-114">參數</span><span class="sxs-lookup"><span data-stu-id="c9bf9-114">PARAMETERS</span></span>

### <span data-ttu-id="c9bf9-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c9bf9-115">-InformationAction</span></span>
<span data-ttu-id="c9bf9-116">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="c9bf9-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c9bf9-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c9bf9-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c9bf9-118">持續</span><span class="sxs-lookup"><span data-stu-id="c9bf9-118">Continue</span></span>
- <span data-ttu-id="c9bf9-119">理會</span><span class="sxs-lookup"><span data-stu-id="c9bf9-119">Ignore</span></span>
- <span data-ttu-id="c9bf9-120">看</span><span class="sxs-lookup"><span data-stu-id="c9bf9-120">Inquire</span></span>
- <span data-ttu-id="c9bf9-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c9bf9-121">SilentlyContinue</span></span>
- <span data-ttu-id="c9bf9-122">停止</span><span class="sxs-lookup"><span data-stu-id="c9bf9-122">Stop</span></span>
- <span data-ttu-id="c9bf9-123">封存</span><span class="sxs-lookup"><span data-stu-id="c9bf9-123">Suspend</span></span>

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

### <span data-ttu-id="c9bf9-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c9bf9-124">-InformationVariable</span></span>
<span data-ttu-id="c9bf9-125">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="c9bf9-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c9bf9-126">-設定檔</span><span class="sxs-lookup"><span data-stu-id="c9bf9-126">-Profile</span></span>
<span data-ttu-id="c9bf9-127">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="c9bf9-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c9bf9-128">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="c9bf9-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c9bf9-129">-角色</span><span class="sxs-lookup"><span data-stu-id="c9bf9-129">-Role</span></span>
<span data-ttu-id="c9bf9-130">指定要指定其遠端桌面設定的選擇性角色陣列。</span><span class="sxs-lookup"><span data-stu-id="c9bf9-130">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="c9bf9-131">如果未指定，則會將 AD 網域設定套用為所有角色的預設配置。</span><span class="sxs-lookup"><span data-stu-id="c9bf9-131">If not specified, the AD domain configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="c9bf9-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c9bf9-132">-ServiceName</span></span>
<span data-ttu-id="c9bf9-133">指定 Azure 服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="c9bf9-133">Specifies the name of an Azure service.</span></span>

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

### <span data-ttu-id="c9bf9-134">-槽</span><span class="sxs-lookup"><span data-stu-id="c9bf9-134">-Slot</span></span>
<span data-ttu-id="c9bf9-135">指定要修改的部署環境。</span><span class="sxs-lookup"><span data-stu-id="c9bf9-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="c9bf9-136">有效值為： [生產] 或 [轉移]。</span><span class="sxs-lookup"><span data-stu-id="c9bf9-136">Valid values are: Production or Staging.</span></span>

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

### <span data-ttu-id="c9bf9-137">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9bf9-137">-UninstallConfiguration</span></span>
<span data-ttu-id="c9bf9-138">表示此 Cmdlet 會從雲端服務卸載所有 AD 網域設定。</span><span class="sxs-lookup"><span data-stu-id="c9bf9-138">Indicates that this cmdlet uninstalls all AD domain configurations from the cloud service.</span></span>

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

### <span data-ttu-id="c9bf9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9bf9-139">CommonParameters</span></span>
<span data-ttu-id="c9bf9-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c9bf9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9bf9-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c9bf9-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9bf9-142">輸入</span><span class="sxs-lookup"><span data-stu-id="c9bf9-142">INPUTS</span></span>

## <span data-ttu-id="c9bf9-143">輸出</span><span class="sxs-lookup"><span data-stu-id="c9bf9-143">OUTPUTS</span></span>

## <span data-ttu-id="c9bf9-144">筆記</span><span class="sxs-lookup"><span data-stu-id="c9bf9-144">NOTES</span></span>

## <span data-ttu-id="c9bf9-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="c9bf9-145">RELATED LINKS</span></span>

[<span data-ttu-id="c9bf9-146">AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="c9bf9-146">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="c9bf9-147">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="c9bf9-147">Set-AzureServiceADDomainExtension</span></span>](./Set-AzureServiceADDomainExtension.md)



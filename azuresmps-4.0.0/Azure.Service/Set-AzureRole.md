---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8170AEF9-46E6-4087-8A68-29DFD5D014B5
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb63d143ca2cafce92109e17fd3ced6a9dc070e8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967270"
---
# <span data-ttu-id="fdbb0-101">Set-AzureRole</span><span class="sxs-lookup"><span data-stu-id="fdbb0-101">Set-AzureRole</span></span>

## <span data-ttu-id="fdbb0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fdbb0-102">SYNOPSIS</span></span>
<span data-ttu-id="fdbb0-103">設定要執行之 Azure 角色的實例數。</span><span class="sxs-lookup"><span data-stu-id="fdbb0-103">Sets the number of instances of an Azure role to run.</span></span>

## <span data-ttu-id="fdbb0-104">句法</span><span class="sxs-lookup"><span data-stu-id="fdbb0-104">SYNTAX</span></span>

```
Set-AzureRole [-ServiceName] <String> [-Slot] <String> [-RoleName] <String> [-Count] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="fdbb0-105">說明</span><span class="sxs-lookup"><span data-stu-id="fdbb0-105">DESCRIPTION</span></span>
<span data-ttu-id="fdbb0-106">**AzureRole** Cmdlet 會將指定角色的實例數設定為在 Azure 部署中執行。</span><span class="sxs-lookup"><span data-stu-id="fdbb0-106">The **Set-AzureRole** cmdlet sets the number of instances of a specified role to run in an Azure deployment.</span></span>

## <span data-ttu-id="fdbb0-107">示例</span><span class="sxs-lookup"><span data-stu-id="fdbb0-107">EXAMPLES</span></span>

### <span data-ttu-id="fdbb0-108">1：設定角色的實例數</span><span class="sxs-lookup"><span data-stu-id="fdbb0-108">1: Set the number of instances for a role</span></span>
```
PS C:\> Set-AzureRole -ServiceName "MySvc01" -Slot "Production" -RoleName "MyTestRole03" -Count 3
```

<span data-ttu-id="fdbb0-109">這個命令會將在生產環境中執行的 MyTestRole03 角色設定為三個實例。</span><span class="sxs-lookup"><span data-stu-id="fdbb0-109">This command sets the MyTestRole03 role that is running in production on the MySvc01 service to have three instances.</span></span>

## <span data-ttu-id="fdbb0-110">參數</span><span class="sxs-lookup"><span data-stu-id="fdbb0-110">PARAMETERS</span></span>

### <span data-ttu-id="fdbb0-111">-Count</span><span class="sxs-lookup"><span data-stu-id="fdbb0-111">-Count</span></span>
<span data-ttu-id="fdbb0-112">指定要執行的角色實例數。</span><span class="sxs-lookup"><span data-stu-id="fdbb0-112">Specifies the number of role instances to run.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdbb0-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="fdbb0-113">-InformationAction</span></span>
<span data-ttu-id="fdbb0-114">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="fdbb0-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fdbb0-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="fdbb0-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fdbb0-116">持續</span><span class="sxs-lookup"><span data-stu-id="fdbb0-116">Continue</span></span>
- <span data-ttu-id="fdbb0-117">理會</span><span class="sxs-lookup"><span data-stu-id="fdbb0-117">Ignore</span></span>
- <span data-ttu-id="fdbb0-118">看</span><span class="sxs-lookup"><span data-stu-id="fdbb0-118">Inquire</span></span>
- <span data-ttu-id="fdbb0-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fdbb0-119">SilentlyContinue</span></span>
- <span data-ttu-id="fdbb0-120">停止</span><span class="sxs-lookup"><span data-stu-id="fdbb0-120">Stop</span></span>
- <span data-ttu-id="fdbb0-121">封存</span><span class="sxs-lookup"><span data-stu-id="fdbb0-121">Suspend</span></span>

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

### <span data-ttu-id="fdbb0-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fdbb0-122">-InformationVariable</span></span>
<span data-ttu-id="fdbb0-123">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="fdbb0-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fdbb0-124">-設定檔</span><span class="sxs-lookup"><span data-stu-id="fdbb0-124">-Profile</span></span>
<span data-ttu-id="fdbb0-125">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="fdbb0-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fdbb0-126">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="fdbb0-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fdbb0-127">-擁有方</span><span class="sxs-lookup"><span data-stu-id="fdbb0-127">-RoleName</span></span>
<span data-ttu-id="fdbb0-128">指定要設定實例數的角色名稱。</span><span class="sxs-lookup"><span data-stu-id="fdbb0-128">Specifies the name of the role for which to set the number of instances.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbb0-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="fdbb0-129">-ServiceName</span></span>
<span data-ttu-id="fdbb0-130">指定 Azure 服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="fdbb0-130">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="fdbb0-131">-槽</span><span class="sxs-lookup"><span data-stu-id="fdbb0-131">-Slot</span></span>
<span data-ttu-id="fdbb0-132">指定要修改之部署的部署環境。</span><span class="sxs-lookup"><span data-stu-id="fdbb0-132">Specifies the deployment environment of the deployment to modify.</span></span>
<span data-ttu-id="fdbb0-133">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="fdbb0-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fdbb0-134">出具</span><span class="sxs-lookup"><span data-stu-id="fdbb0-134">Production</span></span>
- <span data-ttu-id="fdbb0-135">播放</span><span class="sxs-lookup"><span data-stu-id="fdbb0-135">Staging</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbb0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdbb0-136">CommonParameters</span></span>
<span data-ttu-id="fdbb0-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fdbb0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdbb0-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fdbb0-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdbb0-139">輸入</span><span class="sxs-lookup"><span data-stu-id="fdbb0-139">INPUTS</span></span>

## <span data-ttu-id="fdbb0-140">輸出</span><span class="sxs-lookup"><span data-stu-id="fdbb0-140">OUTPUTS</span></span>

## <span data-ttu-id="fdbb0-141">筆記</span><span class="sxs-lookup"><span data-stu-id="fdbb0-141">NOTES</span></span>

## <span data-ttu-id="fdbb0-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="fdbb0-142">RELATED LINKS</span></span>

[<span data-ttu-id="fdbb0-143">AzureRole</span><span class="sxs-lookup"><span data-stu-id="fdbb0-143">Get-AzureRole</span></span>](./Get-AzureRole.md)



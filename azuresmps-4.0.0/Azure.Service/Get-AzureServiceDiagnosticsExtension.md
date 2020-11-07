---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 235DD5D7-BE24-4FBE-88E2-40D1943ED155
online version: ''
schema: 2.0.0
ms.openlocfilehash: e4fb3f35bc64a1431550d4da5aa669e934cd3a7f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967049"
---
# <span data-ttu-id="83857-101">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="83857-101">Get-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="83857-102">摘要</span><span class="sxs-lookup"><span data-stu-id="83857-102">SYNOPSIS</span></span>
<span data-ttu-id="83857-103">取得在特定部署槽中針對所有角色或命名角色套用的雲端服務診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="83857-103">Gets the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="83857-104">句法</span><span class="sxs-lookup"><span data-stu-id="83857-104">SYNTAX</span></span>

```
Get-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="83857-105">說明</span><span class="sxs-lookup"><span data-stu-id="83857-105">DESCRIPTION</span></span>
<span data-ttu-id="83857-106">AzureServiceDiagnosticsExtension Cmdlet 會針對特定部署槽中的所有角色或命名角色， **取得** 雲端服務診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="83857-106">The **Get-AzureServiceDiagnosticsExtension** cmdlet gets the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="83857-107">示例</span><span class="sxs-lookup"><span data-stu-id="83857-107">EXAMPLES</span></span>

### <span data-ttu-id="83857-108">範例1：取得服務診斷延伸</span><span class="sxs-lookup"><span data-stu-id="83857-108">Example 1: Get service diagnostics extension</span></span> 
```
PS C:\> Get-AzureServiceDiagnosticsExtension -ServiceName $Svc
```

<span data-ttu-id="83857-109">這個命令會在所有角色中取得服務的服務診斷。</span><span class="sxs-lookup"><span data-stu-id="83857-109">This command gets the service diagnostics for a service, across all roles.</span></span>

## <span data-ttu-id="83857-110">參數</span><span class="sxs-lookup"><span data-stu-id="83857-110">PARAMETERS</span></span>

### <span data-ttu-id="83857-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="83857-111">-InformationAction</span></span>
<span data-ttu-id="83857-112">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="83857-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="83857-113">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="83857-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="83857-114">持續</span><span class="sxs-lookup"><span data-stu-id="83857-114">Continue</span></span>
- <span data-ttu-id="83857-115">理會</span><span class="sxs-lookup"><span data-stu-id="83857-115">Ignore</span></span>
- <span data-ttu-id="83857-116">看</span><span class="sxs-lookup"><span data-stu-id="83857-116">Inquire</span></span>
- <span data-ttu-id="83857-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="83857-117">SilentlyContinue</span></span>
- <span data-ttu-id="83857-118">停止</span><span class="sxs-lookup"><span data-stu-id="83857-118">Stop</span></span>
- <span data-ttu-id="83857-119">封存</span><span class="sxs-lookup"><span data-stu-id="83857-119">Suspend</span></span>

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

### <span data-ttu-id="83857-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="83857-120">-InformationVariable</span></span>
<span data-ttu-id="83857-121">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="83857-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="83857-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="83857-122">-Profile</span></span>
<span data-ttu-id="83857-123">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="83857-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="83857-124">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="83857-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="83857-125">-角色</span><span class="sxs-lookup"><span data-stu-id="83857-125">-Role</span></span>
<span data-ttu-id="83857-126">指定角色陣列。</span><span class="sxs-lookup"><span data-stu-id="83857-126">Specifies an array of roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83857-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="83857-127">-ServiceName</span></span>
<span data-ttu-id="83857-128">指定部署的 Azure 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="83857-128">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="83857-129">-槽</span><span class="sxs-lookup"><span data-stu-id="83857-129">-Slot</span></span>
<span data-ttu-id="83857-130">指定要修改的部署環境。</span><span class="sxs-lookup"><span data-stu-id="83857-130">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="83857-131">此參數可接受的值為： [生產] 或 [轉移]。</span><span class="sxs-lookup"><span data-stu-id="83857-131">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="83857-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83857-132">CommonParameters</span></span>
<span data-ttu-id="83857-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="83857-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83857-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="83857-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83857-135">輸入</span><span class="sxs-lookup"><span data-stu-id="83857-135">INPUTS</span></span>

## <span data-ttu-id="83857-136">輸出</span><span class="sxs-lookup"><span data-stu-id="83857-136">OUTPUTS</span></span>

## <span data-ttu-id="83857-137">筆記</span><span class="sxs-lookup"><span data-stu-id="83857-137">NOTES</span></span>

## <span data-ttu-id="83857-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="83857-138">RELATED LINKS</span></span>

[<span data-ttu-id="83857-139">移除-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="83857-139">Remove-AzureServiceDiagnosticsExtension</span></span>](./Remove-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="83857-140">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="83857-140">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)



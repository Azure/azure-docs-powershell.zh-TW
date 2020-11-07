---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D08CB0A0-A0A9-4E0A-B1AB-A19A655B501B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5fd66813dcfc08f5e2f5276c4019443f9166945d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967042"
---
# <span data-ttu-id="305b6-101">Get-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="305b6-101">Get-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="305b6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="305b6-102">SYNOPSIS</span></span>
<span data-ttu-id="305b6-103">這個 Cmdlet 會取得在特定部署槽中的所有角色或命名角色上套用的雲端服務遠端桌面延伸。</span><span class="sxs-lookup"><span data-stu-id="305b6-103">This cmdlet gets the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="305b6-104">句法</span><span class="sxs-lookup"><span data-stu-id="305b6-104">SYNTAX</span></span>

```
Get-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="305b6-105">說明</span><span class="sxs-lookup"><span data-stu-id="305b6-105">DESCRIPTION</span></span>
<span data-ttu-id="305b6-106">AzureServiceRemoteDesktopExtension Cmdlet 會針對特定部署槽中的所有角色或命名角色， **取得** 雲端服務遠端桌面延伸。</span><span class="sxs-lookup"><span data-stu-id="305b6-106">The **Get-AzureServiceRemoteDesktopExtension** cmdlet gets the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="305b6-107">示例</span><span class="sxs-lookup"><span data-stu-id="305b6-107">EXAMPLES</span></span>

### <span data-ttu-id="305b6-108">範例1：取得指定服務的遠端桌面延伸</span><span class="sxs-lookup"><span data-stu-id="305b6-108">Example 1: Get remote desktop extension for the specified service</span></span>
```
PS C:\> Get-AzureServiceRemoteDesktopExtension -ServiceName $svc
```

<span data-ttu-id="305b6-109">這個命令會取得指定服務的遠端桌面延伸。</span><span class="sxs-lookup"><span data-stu-id="305b6-109">This command gets the remote desktop extension for the specified service.</span></span>

## <span data-ttu-id="305b6-110">參數</span><span class="sxs-lookup"><span data-stu-id="305b6-110">PARAMETERS</span></span>

### <span data-ttu-id="305b6-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="305b6-111">-InformationAction</span></span>
<span data-ttu-id="305b6-112">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="305b6-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="305b6-113">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="305b6-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="305b6-114">持續</span><span class="sxs-lookup"><span data-stu-id="305b6-114">Continue</span></span>
- <span data-ttu-id="305b6-115">理會</span><span class="sxs-lookup"><span data-stu-id="305b6-115">Ignore</span></span>
- <span data-ttu-id="305b6-116">看</span><span class="sxs-lookup"><span data-stu-id="305b6-116">Inquire</span></span>
- <span data-ttu-id="305b6-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="305b6-117">SilentlyContinue</span></span>
- <span data-ttu-id="305b6-118">停止</span><span class="sxs-lookup"><span data-stu-id="305b6-118">Stop</span></span>
- <span data-ttu-id="305b6-119">封存</span><span class="sxs-lookup"><span data-stu-id="305b6-119">Suspend</span></span>

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

### <span data-ttu-id="305b6-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="305b6-120">-InformationVariable</span></span>
<span data-ttu-id="305b6-121">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="305b6-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="305b6-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="305b6-122">-Profile</span></span>
<span data-ttu-id="305b6-123">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="305b6-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="305b6-124">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="305b6-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="305b6-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="305b6-125">-ServiceName</span></span>
<span data-ttu-id="305b6-126">指定部署的 Azure 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="305b6-126">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="305b6-127">-槽</span><span class="sxs-lookup"><span data-stu-id="305b6-127">-Slot</span></span>
<span data-ttu-id="305b6-128">指定要修改的部署環境。</span><span class="sxs-lookup"><span data-stu-id="305b6-128">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="305b6-129">此參數可接受的值為： [生產] 或 [轉移]。</span><span class="sxs-lookup"><span data-stu-id="305b6-129">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="305b6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="305b6-130">CommonParameters</span></span>
<span data-ttu-id="305b6-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="305b6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="305b6-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="305b6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="305b6-133">輸入</span><span class="sxs-lookup"><span data-stu-id="305b6-133">INPUTS</span></span>

## <span data-ttu-id="305b6-134">輸出</span><span class="sxs-lookup"><span data-stu-id="305b6-134">OUTPUTS</span></span>

## <span data-ttu-id="305b6-135">筆記</span><span class="sxs-lookup"><span data-stu-id="305b6-135">NOTES</span></span>

## <span data-ttu-id="305b6-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="305b6-136">RELATED LINKS</span></span>

[<span data-ttu-id="305b6-137">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="305b6-137">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)



---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2171943B-D1AC-45FD-99FD-DD0C14AFC60C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 38990d3084cf5f494dc811ec6fe458003b8313c9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967801"
---
# <span data-ttu-id="8f179-101">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="8f179-101">Get-AzureDeployment</span></span>

## <span data-ttu-id="8f179-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8f179-102">SYNOPSIS</span></span>
<span data-ttu-id="8f179-103">取得部署的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8f179-103">Gets details of a deployment.</span></span>

## <span data-ttu-id="8f179-104">句法</span><span class="sxs-lookup"><span data-stu-id="8f179-104">SYNTAX</span></span>

```
Get-AzureDeployment [-ServiceName] <String> [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8f179-105">說明</span><span class="sxs-lookup"><span data-stu-id="8f179-105">DESCRIPTION</span></span>
<span data-ttu-id="8f179-106">**AzureDeployment** Cmdlet 會取得 Azure 部署的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8f179-106">The **Get-AzureDeployment** cmdlet gets details of an Azure deployment.</span></span>
<span data-ttu-id="8f179-107">指定 Azure 服務的名稱和部署的槽。</span><span class="sxs-lookup"><span data-stu-id="8f179-107">Specify the name of the Azure service and the slot of the deployment.</span></span>

## <span data-ttu-id="8f179-108">示例</span><span class="sxs-lookup"><span data-stu-id="8f179-108">EXAMPLES</span></span>

### <span data-ttu-id="8f179-109">範例1：取得生產部署的詳細資料</span><span class="sxs-lookup"><span data-stu-id="8f179-109">Example 1: Get details for a production deployment</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="8f179-110">這個命令會傳回名為 ContosoService 的服務部署的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8f179-110">This command returns the details of the deployment for the service named ContosoService.</span></span>
<span data-ttu-id="8f179-111">這個命令不會指定槽。</span><span class="sxs-lookup"><span data-stu-id="8f179-111">This command does not specify a slot.</span></span>
<span data-ttu-id="8f179-112">因此，命令會使用「生產」的預設值。</span><span class="sxs-lookup"><span data-stu-id="8f179-112">Therefore, the command uses the default value of Production.</span></span>

### <span data-ttu-id="8f179-113">範例2：取得分段部署的詳細資料</span><span class="sxs-lookup"><span data-stu-id="8f179-113">Example 2: Get details for a staging deployment</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService" -Slot "Staging"
```

<span data-ttu-id="8f179-114">這個命令會傳回 ContosoService 的過渡部署詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8f179-114">This command returns the details of the staging deployment of ContosoService.</span></span>

## <span data-ttu-id="8f179-115">參數</span><span class="sxs-lookup"><span data-stu-id="8f179-115">PARAMETERS</span></span>

### <span data-ttu-id="8f179-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8f179-116">-InformationAction</span></span>
<span data-ttu-id="8f179-117">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="8f179-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8f179-118">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="8f179-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8f179-119">持續</span><span class="sxs-lookup"><span data-stu-id="8f179-119">Continue</span></span>
- <span data-ttu-id="8f179-120">理會</span><span class="sxs-lookup"><span data-stu-id="8f179-120">Ignore</span></span>
- <span data-ttu-id="8f179-121">看</span><span class="sxs-lookup"><span data-stu-id="8f179-121">Inquire</span></span>
- <span data-ttu-id="8f179-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8f179-122">SilentlyContinue</span></span>
- <span data-ttu-id="8f179-123">停止</span><span class="sxs-lookup"><span data-stu-id="8f179-123">Stop</span></span>
- <span data-ttu-id="8f179-124">封存</span><span class="sxs-lookup"><span data-stu-id="8f179-124">Suspend</span></span>

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

### <span data-ttu-id="8f179-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8f179-125">-InformationVariable</span></span>
<span data-ttu-id="8f179-126">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="8f179-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8f179-127">-設定檔</span><span class="sxs-lookup"><span data-stu-id="8f179-127">-Profile</span></span>
<span data-ttu-id="8f179-128">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="8f179-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8f179-129">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="8f179-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8f179-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8f179-130">-ServiceName</span></span>
<span data-ttu-id="8f179-131">指定服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f179-131">Specifies the name of the service.</span></span>

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

### <span data-ttu-id="8f179-132">-槽</span><span class="sxs-lookup"><span data-stu-id="8f179-132">-Slot</span></span>
<span data-ttu-id="8f179-133">指定部署的環境。</span><span class="sxs-lookup"><span data-stu-id="8f179-133">Specifies the environment of the deployment.</span></span>
<span data-ttu-id="8f179-134">有效值為：分段或生產。</span><span class="sxs-lookup"><span data-stu-id="8f179-134">Valid values are: Staging or Production.</span></span>
<span data-ttu-id="8f179-135">預設值為 [生產]。</span><span class="sxs-lookup"><span data-stu-id="8f179-135">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f179-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f179-136">CommonParameters</span></span>
<span data-ttu-id="8f179-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8f179-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f179-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8f179-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f179-139">輸入</span><span class="sxs-lookup"><span data-stu-id="8f179-139">INPUTS</span></span>

## <span data-ttu-id="8f179-140">輸出</span><span class="sxs-lookup"><span data-stu-id="8f179-140">OUTPUTS</span></span>

## <span data-ttu-id="8f179-141">筆記</span><span class="sxs-lookup"><span data-stu-id="8f179-141">NOTES</span></span>

## <span data-ttu-id="8f179-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f179-142">RELATED LINKS</span></span>

[<span data-ttu-id="8f179-143">AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="8f179-143">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="8f179-144">移動流覽 AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="8f179-144">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="8f179-145">新-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="8f179-145">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="8f179-146">移除-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="8f179-146">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="8f179-147">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="8f179-147">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)



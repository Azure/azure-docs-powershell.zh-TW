---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B935B615-1200-4A83-95AF-4F17785793B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: a331f3e0ff2797b84c241e64872e3af0841cb106
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967690"
---
# <span data-ttu-id="ffbb5-101">Move-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="ffbb5-101">Move-AzureDeployment</span></span>

## <span data-ttu-id="ffbb5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ffbb5-102">SYNOPSIS</span></span>
<span data-ttu-id="ffbb5-103">在生產與轉移之間的交換部署。</span><span class="sxs-lookup"><span data-stu-id="ffbb5-103">Swaps deployments between production and staging.</span></span>

## <span data-ttu-id="ffbb5-104">句法</span><span class="sxs-lookup"><span data-stu-id="ffbb5-104">SYNTAX</span></span>

```
Move-AzureDeployment [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ffbb5-105">說明</span><span class="sxs-lookup"><span data-stu-id="ffbb5-105">DESCRIPTION</span></span>
<span data-ttu-id="ffbb5-106">**AzureDeployment** Cmdlet 會交換生產與暫存環境中的部署虛擬 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ffbb5-106">The **Move-AzureDeployment** cmdlet swaps the virtual IP addresses of deployments in production and staging environments.</span></span>
<span data-ttu-id="ffbb5-107">這個 Cmdlet 會將目前在轉移環境中執行的部署交換到生產環境，以及在生產環境中執行的部署到暫存環境。</span><span class="sxs-lookup"><span data-stu-id="ffbb5-107">This cmdlet swaps a deployment that currently runs in the staging environment to the production environment, and a deployment that runs in the production environment to the staging environment.</span></span>
<span data-ttu-id="ffbb5-108">如果在暫存環境中有部署且生產環境中沒有部署，則此 Cmdlet 會將部署移至生產環境。</span><span class="sxs-lookup"><span data-stu-id="ffbb5-108">If there is a deployment in the staging environment and no deployment in the production environment, the cmdlet moves the deployment to production.</span></span>
<span data-ttu-id="ffbb5-109">如果在生產環境中有部署，且在轉移環境中沒有部署，則 Cmdlet 會失敗。</span><span class="sxs-lookup"><span data-stu-id="ffbb5-109">If there is a deployment in the production environment and no deployment in the staging environment, the cmdlet fails.</span></span>

## <span data-ttu-id="ffbb5-110">示例</span><span class="sxs-lookup"><span data-stu-id="ffbb5-110">EXAMPLES</span></span>

### <span data-ttu-id="ffbb5-111">範例1：交換服務的部署</span><span class="sxs-lookup"><span data-stu-id="ffbb5-111">Example 1: Swap deployments for a service</span></span>
```
PS C:\> Move-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="ffbb5-112">這個命令會在生產與轉移環境之間，交換名為 ContosoService 的服務部署。</span><span class="sxs-lookup"><span data-stu-id="ffbb5-112">This command swaps the deployments of the service named ContosoService between the production and staging environments.</span></span>

## <span data-ttu-id="ffbb5-113">參數</span><span class="sxs-lookup"><span data-stu-id="ffbb5-113">PARAMETERS</span></span>

### <span data-ttu-id="ffbb5-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ffbb5-114">-InformationAction</span></span>
<span data-ttu-id="ffbb5-115">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="ffbb5-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ffbb5-116">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ffbb5-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ffbb5-117">持續</span><span class="sxs-lookup"><span data-stu-id="ffbb5-117">Continue</span></span>
- <span data-ttu-id="ffbb5-118">理會</span><span class="sxs-lookup"><span data-stu-id="ffbb5-118">Ignore</span></span>
- <span data-ttu-id="ffbb5-119">看</span><span class="sxs-lookup"><span data-stu-id="ffbb5-119">Inquire</span></span>
- <span data-ttu-id="ffbb5-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ffbb5-120">SilentlyContinue</span></span>
- <span data-ttu-id="ffbb5-121">停止</span><span class="sxs-lookup"><span data-stu-id="ffbb5-121">Stop</span></span>
- <span data-ttu-id="ffbb5-122">封存</span><span class="sxs-lookup"><span data-stu-id="ffbb5-122">Suspend</span></span>

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

### <span data-ttu-id="ffbb5-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ffbb5-123">-InformationVariable</span></span>
<span data-ttu-id="ffbb5-124">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="ffbb5-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ffbb5-125">-設定檔</span><span class="sxs-lookup"><span data-stu-id="ffbb5-125">-Profile</span></span>
<span data-ttu-id="ffbb5-126">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="ffbb5-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ffbb5-127">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="ffbb5-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ffbb5-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ffbb5-128">-ServiceName</span></span>
<span data-ttu-id="ffbb5-129">指定此 Cmdlet 要調換生產與暫存部署的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="ffbb5-129">Specifies the name of the service for which this cmdlet swaps production and staging deployments.</span></span>

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

### <span data-ttu-id="ffbb5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffbb5-130">CommonParameters</span></span>
<span data-ttu-id="ffbb5-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ffbb5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffbb5-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ffbb5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffbb5-133">輸入</span><span class="sxs-lookup"><span data-stu-id="ffbb5-133">INPUTS</span></span>

## <span data-ttu-id="ffbb5-134">輸出</span><span class="sxs-lookup"><span data-stu-id="ffbb5-134">OUTPUTS</span></span>

### <span data-ttu-id="ffbb5-135">ManagementOperationCoNtext</span><span class="sxs-lookup"><span data-stu-id="ffbb5-135">ManagementOperationContext</span></span>

## <span data-ttu-id="ffbb5-136">筆記</span><span class="sxs-lookup"><span data-stu-id="ffbb5-136">NOTES</span></span>

## <span data-ttu-id="ffbb5-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="ffbb5-137">RELATED LINKS</span></span>

[<span data-ttu-id="ffbb5-138">AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="ffbb5-138">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="ffbb5-139">AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="ffbb5-139">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="ffbb5-140">新-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="ffbb5-140">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="ffbb5-141">移除-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="ffbb5-141">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="ffbb5-142">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="ffbb5-142">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)



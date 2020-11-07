---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3F3BC5AF-8D7B-40BF-A072-A11C7BDCB6B3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09adc7e9b2faf9b9a905fa1c94fb6526e02c110f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967232"
---
# <span data-ttu-id="c66e6-101">Set-AzureWalkUpgradeDomain</span><span class="sxs-lookup"><span data-stu-id="c66e6-101">Set-AzureWalkUpgradeDomain</span></span>

## <span data-ttu-id="c66e6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c66e6-102">SYNOPSIS</span></span>
<span data-ttu-id="c66e6-103">遍歷指定的升級網域。</span><span class="sxs-lookup"><span data-stu-id="c66e6-103">Walks the specified upgrade domain.</span></span>

## <span data-ttu-id="c66e6-104">句法</span><span class="sxs-lookup"><span data-stu-id="c66e6-104">SYNTAX</span></span>

```
Set-AzureWalkUpgradeDomain [-ServiceName] <String> [-Slot] <String> [-DomainNumber] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="c66e6-105">說明</span><span class="sxs-lookup"><span data-stu-id="c66e6-105">DESCRIPTION</span></span>
<span data-ttu-id="c66e6-106">**AzureWalkUpgradeDomain** Cmdlet 會初始化 Azure 部署的實際升級。</span><span class="sxs-lookup"><span data-stu-id="c66e6-106">The **Set-AzureWalkUpgradeDomain** cmdlet initiates the actual upgrade of an Azure deployment.</span></span>
<span data-ttu-id="c66e6-107">升級套件和設定是使用 **AzureDeployment** Cmdlet 與-升級開關進行設定。</span><span class="sxs-lookup"><span data-stu-id="c66e6-107">The upgrade package and configuration are set by using the **Set-AzureDeployment** cmdlet with the -Upgrade switch.</span></span>

## <span data-ttu-id="c66e6-108">示例</span><span class="sxs-lookup"><span data-stu-id="c66e6-108">EXAMPLES</span></span>

### <span data-ttu-id="c66e6-109">範例1：啟動生產部署的升級</span><span class="sxs-lookup"><span data-stu-id="c66e6-109">Example 1: Initiate an upgrade of a production deployment</span></span>
```
PS C:\> Set-AzureWalkUpgradeDomain -ServiceName "MySvc1" -slot "Production" -UpgradeDomain 2
```

<span data-ttu-id="c66e6-110">這個命令會啟動 MySvc1 服務生產部署的升級網域2升級。</span><span class="sxs-lookup"><span data-stu-id="c66e6-110">This command initiates the upgrade of Upgrade Domain 2 of the production deployment of the MySvc1 service.</span></span>

## <span data-ttu-id="c66e6-111">參數</span><span class="sxs-lookup"><span data-stu-id="c66e6-111">PARAMETERS</span></span>

### <span data-ttu-id="c66e6-112">-DomainNumber</span><span class="sxs-lookup"><span data-stu-id="c66e6-112">-DomainNumber</span></span>
<span data-ttu-id="c66e6-113">指定升級網域以進行升級。</span><span class="sxs-lookup"><span data-stu-id="c66e6-113">Specifies the upgrade domain to upgrade.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c66e6-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c66e6-114">-InformationAction</span></span>
<span data-ttu-id="c66e6-115">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="c66e6-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c66e6-116">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c66e6-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c66e6-117">持續</span><span class="sxs-lookup"><span data-stu-id="c66e6-117">Continue</span></span>
- <span data-ttu-id="c66e6-118">理會</span><span class="sxs-lookup"><span data-stu-id="c66e6-118">Ignore</span></span>
- <span data-ttu-id="c66e6-119">看</span><span class="sxs-lookup"><span data-stu-id="c66e6-119">Inquire</span></span>
- <span data-ttu-id="c66e6-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c66e6-120">SilentlyContinue</span></span>
- <span data-ttu-id="c66e6-121">停止</span><span class="sxs-lookup"><span data-stu-id="c66e6-121">Stop</span></span>
- <span data-ttu-id="c66e6-122">封存</span><span class="sxs-lookup"><span data-stu-id="c66e6-122">Suspend</span></span>

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

### <span data-ttu-id="c66e6-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c66e6-123">-InformationVariable</span></span>
<span data-ttu-id="c66e6-124">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="c66e6-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c66e6-125">-設定檔</span><span class="sxs-lookup"><span data-stu-id="c66e6-125">-Profile</span></span>
<span data-ttu-id="c66e6-126">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="c66e6-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c66e6-127">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="c66e6-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c66e6-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c66e6-128">-ServiceName</span></span>
<span data-ttu-id="c66e6-129">指定要升級的 Microsoft Azure 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="c66e6-129">Specifies the Microsoft Azure service name to upgrade.</span></span>

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

### <span data-ttu-id="c66e6-130">-槽</span><span class="sxs-lookup"><span data-stu-id="c66e6-130">-Slot</span></span>
<span data-ttu-id="c66e6-131">指定要升級的部署環境。</span><span class="sxs-lookup"><span data-stu-id="c66e6-131">Specifies the environment of the deployment to upgrade.</span></span>

<span data-ttu-id="c66e6-132">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c66e6-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c66e6-133">播放</span><span class="sxs-lookup"><span data-stu-id="c66e6-133">Staging</span></span>
- <span data-ttu-id="c66e6-134">出具</span><span class="sxs-lookup"><span data-stu-id="c66e6-134">Production</span></span>

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

### <span data-ttu-id="c66e6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c66e6-135">CommonParameters</span></span>
<span data-ttu-id="c66e6-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c66e6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c66e6-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c66e6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c66e6-138">輸入</span><span class="sxs-lookup"><span data-stu-id="c66e6-138">INPUTS</span></span>

## <span data-ttu-id="c66e6-139">輸出</span><span class="sxs-lookup"><span data-stu-id="c66e6-139">OUTPUTS</span></span>

### <span data-ttu-id="c66e6-140">ManagementOperationCoNtext</span><span class="sxs-lookup"><span data-stu-id="c66e6-140">ManagementOperationContext</span></span>

## <span data-ttu-id="c66e6-141">筆記</span><span class="sxs-lookup"><span data-stu-id="c66e6-141">NOTES</span></span>

## <span data-ttu-id="c66e6-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="c66e6-142">RELATED LINKS</span></span>

[<span data-ttu-id="c66e6-143">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="c66e6-143">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)



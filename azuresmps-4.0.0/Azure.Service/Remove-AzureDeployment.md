---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D6D54096-670D-43E4-93EB-24C8FBA199A4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2db1d7a6bc87c694cf06ea1fef0a886c61734a75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967611"
---
# <span data-ttu-id="909ab-101">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="909ab-101">Remove-AzureDeployment</span></span>

## <span data-ttu-id="909ab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="909ab-102">SYNOPSIS</span></span>
<span data-ttu-id="909ab-103">刪除雲端服務的部署。</span><span class="sxs-lookup"><span data-stu-id="909ab-103">Deletes a deployment of a cloud service.</span></span>

## <span data-ttu-id="909ab-104">句法</span><span class="sxs-lookup"><span data-stu-id="909ab-104">SYNTAX</span></span>

```
Remove-AzureDeployment [-ServiceName] <String> [-Slot] <String> [-DeleteVHD] [-Force]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="909ab-105">說明</span><span class="sxs-lookup"><span data-stu-id="909ab-105">DESCRIPTION</span></span>
<span data-ttu-id="909ab-106">**AzureDeployment** Cmdlet 會刪除 Azure 雲端服務的部署。</span><span class="sxs-lookup"><span data-stu-id="909ab-106">The **Remove-AzureDeployment** cmdlet deletes a deployment of an Azure cloud service.</span></span>
<span data-ttu-id="909ab-107">若要刪除部署，請先將其暫停。</span><span class="sxs-lookup"><span data-stu-id="909ab-107">To delete a deployment, first suspend it.</span></span>

## <span data-ttu-id="909ab-108">示例</span><span class="sxs-lookup"><span data-stu-id="909ab-108">EXAMPLES</span></span>

### <span data-ttu-id="909ab-109">範例1：移除部署</span><span class="sxs-lookup"><span data-stu-id="909ab-109">Example 1: Remove a deployment</span></span>
```
PS C:\> Remove-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="909ab-110">這個命令會移除名為 ContosoService 的 Azure 服務部署。</span><span class="sxs-lookup"><span data-stu-id="909ab-110">This command removes the deployment of the Azure service named ContosoService.</span></span>
<span data-ttu-id="909ab-111">因為這個命令不會指定槽，所以它會從生產環境中移除服務。</span><span class="sxs-lookup"><span data-stu-id="909ab-111">Because this command does not specify a slot, it removes the service from the production environment.</span></span>

### <span data-ttu-id="909ab-112">範例2：移除部署和虛擬硬碟</span><span class="sxs-lookup"><span data-stu-id="909ab-112">Example 2: Remove a deployment and virtual hard disks</span></span>
```
PS C:\> Remove-AzureDeployment -ServiceName "ContosoService" -DeleteVHD
```

<span data-ttu-id="909ab-113">這個命令會從生產環境中移除名為 ContosoService 的服務部署。</span><span class="sxs-lookup"><span data-stu-id="909ab-113">This command removes the deployment of the service named ContosoService from the production environment.</span></span>
<span data-ttu-id="909ab-114">此命令也會移除基礎虛擬硬碟。</span><span class="sxs-lookup"><span data-stu-id="909ab-114">The command also removes the underlying virtual hard disks.</span></span>

## <span data-ttu-id="909ab-115">參數</span><span class="sxs-lookup"><span data-stu-id="909ab-115">PARAMETERS</span></span>

### <span data-ttu-id="909ab-116">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="909ab-116">-DeleteVHD</span></span>
<span data-ttu-id="909ab-117">指定此 Cmdlet 會從 blob 儲存體中移除部署和虛擬硬碟 (Vhd) 。</span><span class="sxs-lookup"><span data-stu-id="909ab-117">Specifies that this cmdlet removes the deployment and the virtual hard disks (VHDs) from blob storage.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="909ab-118">-Force</span><span class="sxs-lookup"><span data-stu-id="909ab-118">-Force</span></span>
<span data-ttu-id="909ab-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="909ab-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="909ab-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="909ab-120">-InformationAction</span></span>
<span data-ttu-id="909ab-121">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="909ab-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="909ab-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="909ab-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="909ab-123">持續</span><span class="sxs-lookup"><span data-stu-id="909ab-123">Continue</span></span>
- <span data-ttu-id="909ab-124">理會</span><span class="sxs-lookup"><span data-stu-id="909ab-124">Ignore</span></span>
- <span data-ttu-id="909ab-125">看</span><span class="sxs-lookup"><span data-stu-id="909ab-125">Inquire</span></span>
- <span data-ttu-id="909ab-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="909ab-126">SilentlyContinue</span></span>
- <span data-ttu-id="909ab-127">停止</span><span class="sxs-lookup"><span data-stu-id="909ab-127">Stop</span></span>
- <span data-ttu-id="909ab-128">封存</span><span class="sxs-lookup"><span data-stu-id="909ab-128">Suspend</span></span>

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

### <span data-ttu-id="909ab-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="909ab-129">-InformationVariable</span></span>
<span data-ttu-id="909ab-130">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="909ab-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="909ab-131">-設定檔</span><span class="sxs-lookup"><span data-stu-id="909ab-131">-Profile</span></span>
<span data-ttu-id="909ab-132">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="909ab-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="909ab-133">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="909ab-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="909ab-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="909ab-134">-ServiceName</span></span>
<span data-ttu-id="909ab-135">指定此 Cmdlet 刪除其部署的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="909ab-135">Specifies the name of the service for which this cmdlet deletes a deployment.</span></span>

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

### <span data-ttu-id="909ab-136">-槽</span><span class="sxs-lookup"><span data-stu-id="909ab-136">-Slot</span></span>
<span data-ttu-id="909ab-137">指定此 Cmdlet 從中刪除部署的部署環境。</span><span class="sxs-lookup"><span data-stu-id="909ab-137">Specifies the deployment environment from which this cmdlet deletes the deployment.</span></span>
<span data-ttu-id="909ab-138">有效值為：暫存與生產。</span><span class="sxs-lookup"><span data-stu-id="909ab-138">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="909ab-139">預設值為 [生產]。</span><span class="sxs-lookup"><span data-stu-id="909ab-139">The default value is Production.</span></span>

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

### <span data-ttu-id="909ab-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="909ab-140">CommonParameters</span></span>
<span data-ttu-id="909ab-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="909ab-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="909ab-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="909ab-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="909ab-143">輸入</span><span class="sxs-lookup"><span data-stu-id="909ab-143">INPUTS</span></span>

## <span data-ttu-id="909ab-144">輸出</span><span class="sxs-lookup"><span data-stu-id="909ab-144">OUTPUTS</span></span>

### <span data-ttu-id="909ab-145">ManagementOperationCoNtext</span><span class="sxs-lookup"><span data-stu-id="909ab-145">ManagementOperationContext</span></span>

## <span data-ttu-id="909ab-146">筆記</span><span class="sxs-lookup"><span data-stu-id="909ab-146">NOTES</span></span>

## <span data-ttu-id="909ab-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="909ab-147">RELATED LINKS</span></span>

[<span data-ttu-id="909ab-148">AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="909ab-148">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="909ab-149">AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="909ab-149">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="909ab-150">移動流覽 AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="909ab-150">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="909ab-151">新-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="909ab-151">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="909ab-152">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="909ab-152">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)



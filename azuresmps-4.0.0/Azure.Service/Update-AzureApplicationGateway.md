---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C7F08804-E177-4BC5-8F0E-DEC1B467C4BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20cb37fbba8fd3789c0932f9ff1e9352334662e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967290"
---
# <span data-ttu-id="d2c0f-101">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d2c0f-101">Update-AzureApplicationGateway</span></span>

## <span data-ttu-id="d2c0f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d2c0f-102">SYNOPSIS</span></span>
<span data-ttu-id="d2c0f-103">更新應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-103">Updates an application gateway.</span></span>

## <span data-ttu-id="d2c0f-104">句法</span><span class="sxs-lookup"><span data-stu-id="d2c0f-104">SYNTAX</span></span>

```
Update-AzureApplicationGateway -Name <String> [-VnetName <String>]
 [-Subnets <System.Collections.Generic.List`1[System.String]>] [-InstanceCount <UInt32>]
 [-GatewaySize <String>] [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d2c0f-105">說明</span><span class="sxs-lookup"><span data-stu-id="d2c0f-105">DESCRIPTION</span></span>
<span data-ttu-id="d2c0f-106">**AzureApplicationGateway** Cmdlet 會更新現有的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-106">The **Update-AzureApplicationGateway** cmdlet updates an existing application gateway.</span></span>

## <span data-ttu-id="d2c0f-107">示例</span><span class="sxs-lookup"><span data-stu-id="d2c0f-107">EXAMPLES</span></span>

### <span data-ttu-id="d2c0f-108">範例1：使用名稱來修改應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="d2c0f-108">Example 1: Modify an application gateway by using its name</span></span>
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork18" -Subnets @("Subnet05", "Subnet06")
```

<span data-ttu-id="d2c0f-109">第一個命令會停止名為 ApplicationGateway06 的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-109">The first command stops the application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="d2c0f-110">您必須先停止應用程式閘道，才能修改虛擬網路或子網。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-110">An application gateway must be stopped before you can modify the virtual network or subnets.</span></span>

<span data-ttu-id="d2c0f-111">第二個命令會修改名為 ApplicationGateway06 的應用程式閘道的虛擬子網和子網。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-111">The second command modifies the virtual subnet and subnets for the application gateway named ApplicationGateway06.</span></span>

### <span data-ttu-id="d2c0f-112">範例2：修改應用程式閘道的其他屬性</span><span class="sxs-lookup"><span data-stu-id="d2c0f-112">Example 2: Modify additional properties of an application gateway</span></span>
```
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -InstanceCount 2 -GatewaySize "Large" -Description "Updated application gateway"
```

<span data-ttu-id="d2c0f-113">這個命令會修改名為 ApplicationGateway06 的應用程式閘道的實例計數、閘道大小及描述。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-113">This command modifies the instance count, gateway size, and description for the application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="d2c0f-114">這個命令不會修改應用程式閘道的虛擬網路或子網。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-114">This command does not modify the virtual network or subnets for the application gateway.</span></span>
<span data-ttu-id="d2c0f-115">因此，在執行這個命令之前，您不需要停止應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-115">Therefore, you do not have to stop the application gateway before you run this command.</span></span>

### <span data-ttu-id="d2c0f-116">範例3：使用管線修改應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="d2c0f-116">Example 3: Modify an application gateway by using the pipeline</span></span>
```
PS C:\> $ApplicationGateway = Get-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> $ApplicationGateway.GatewaySize = "Medium"
PS C:\> $ApplicationGateway | Update-AzureApplicationGateway
```

<span data-ttu-id="d2c0f-117">第一個命令會使用 **AzureApplicationGateway** Cmdlet 取得名為 ApplicationGateway06 的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-117">The first command gets the application gateway named ApplicationGateway06 by using the **Get-AzureApplicationGateway** cmdlet.</span></span>
<span data-ttu-id="d2c0f-118">該命令會將它儲存在 $ApplicationGateway 變數中。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-118">The command stores it in the $ApplicationGateway variable.</span></span>

<span data-ttu-id="d2c0f-119">第二個命令會將 **GatewaySize** 屬性指派為值中。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-119">The second command assigns the **GatewaySize** property the value Medium.</span></span>

<span data-ttu-id="d2c0f-120">最終命令會將更新的 $ApplicationGateway 傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-120">The final command passes the updated $ApplicationGateway to the current cmdlet.</span></span>

## <span data-ttu-id="d2c0f-121">參數</span><span class="sxs-lookup"><span data-stu-id="d2c0f-121">PARAMETERS</span></span>

### <span data-ttu-id="d2c0f-122">-描述</span><span class="sxs-lookup"><span data-stu-id="d2c0f-122">-Description</span></span>
<span data-ttu-id="d2c0f-123">指定此 Cmdlet 指派給應用程式閘道的描述。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-123">Specifies a description that this cmdlet assigns to the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c0f-124">-GatewaySize</span><span class="sxs-lookup"><span data-stu-id="d2c0f-124">-GatewaySize</span></span>
<span data-ttu-id="d2c0f-125">指定此 Cmdlet 指派給應用程式閘道的大小。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-125">Specifies the size that this cmdlet assigns to the application gateway.</span></span>
<span data-ttu-id="d2c0f-126">有效值為：</span><span class="sxs-lookup"><span data-stu-id="d2c0f-126">Valid values are:</span></span>

- <span data-ttu-id="d2c0f-127">小規模</span><span class="sxs-lookup"><span data-stu-id="d2c0f-127">Small</span></span>
- <span data-ttu-id="d2c0f-128">深淺</span><span class="sxs-lookup"><span data-stu-id="d2c0f-128">Medium</span></span>
- <span data-ttu-id="d2c0f-129">大中型</span><span class="sxs-lookup"><span data-stu-id="d2c0f-129">Large</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c0f-130">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="d2c0f-130">-InstanceCount</span></span>
<span data-ttu-id="d2c0f-131">指定此 Cmdlet 指派給應用程式閘道的實例數。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-131">Specifies the number of instances that this cmdlet assigns to the application gateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c0f-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="d2c0f-132">-Name</span></span>
<span data-ttu-id="d2c0f-133">指定此 Cmdlet 更新之應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-133">Specifies the name of the application gateway that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c0f-134">-設定檔</span><span class="sxs-lookup"><span data-stu-id="d2c0f-134">-Profile</span></span>
<span data-ttu-id="d2c0f-135">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d2c0f-136">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d2c0f-137">-子網</span><span class="sxs-lookup"><span data-stu-id="d2c0f-137">-Subnets</span></span>
<span data-ttu-id="d2c0f-138">指定此 Cmdlet 在其中部署應用程式閘道的子網陣列。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-138">Specifies an array of subnets in which this cmdlet deploys the application gateway.</span></span>

<span data-ttu-id="d2c0f-139">當應用程式閘道正在執行時，您無法更新子網。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-139">You cannot update subnets while the application gateway is running.</span></span>
<span data-ttu-id="d2c0f-140">若要停止應用程式閘道，請使用 Stop-AzureApplicationGateway Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-140">To stop the application gateway, use the Stop-AzureApplicationGateway cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c0f-141">-VnetName</span><span class="sxs-lookup"><span data-stu-id="d2c0f-141">-VnetName</span></span>
<span data-ttu-id="d2c0f-142">指定此 Cmdlet 在哪個虛擬網路中部署應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-142">Specifies the virtual network in which this cmdlet deploys the application gateway.</span></span>

<span data-ttu-id="d2c0f-143">當應用程式閘道正在執行時，您無法更新虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-143">You cannot update a virtual network while the application gateway is running.</span></span>
<span data-ttu-id="d2c0f-144">若要停止應用程式閘道，請使用 **停止 AzureApplicationGateway** 。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-144">To stop the application gateway, use **Stop-AzureApplicationGateway**.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c0f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2c0f-145">CommonParameters</span></span>
<span data-ttu-id="d2c0f-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2c0f-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d2c0f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2c0f-148">輸入</span><span class="sxs-lookup"><span data-stu-id="d2c0f-148">INPUTS</span></span>

### <span data-ttu-id="d2c0f-149">System.object</span><span class="sxs-lookup"><span data-stu-id="d2c0f-149">System.String</span></span>

## <span data-ttu-id="d2c0f-150">輸出</span><span class="sxs-lookup"><span data-stu-id="d2c0f-150">OUTPUTS</span></span>

### <span data-ttu-id="d2c0f-151">ApplicationGatewayOperationResponse 的 ApplicationGateway。 WindowsAzure</span><span class="sxs-lookup"><span data-stu-id="d2c0f-151">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="d2c0f-152">筆記</span><span class="sxs-lookup"><span data-stu-id="d2c0f-152">NOTES</span></span>

## <span data-ttu-id="d2c0f-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="d2c0f-153">RELATED LINKS</span></span>

[<span data-ttu-id="d2c0f-154">AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d2c0f-154">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="d2c0f-155">新-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d2c0f-155">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="d2c0f-156">移除-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d2c0f-156">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="d2c0f-157">開始-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d2c0f-157">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="d2c0f-158">停止 AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d2c0f-158">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

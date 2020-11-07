---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BED3D3FE-D1E8-4857-A675-7B2670A129B2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 039afbea4d4eb6736cf3b0faebf189edef2d9c26
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967672"
---
# <span data-ttu-id="e3ebc-101">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3ebc-101">New-AzureApplicationGateway</span></span>

## <span data-ttu-id="e3ebc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3ebc-102">SYNOPSIS</span></span>
<span data-ttu-id="e3ebc-103">建立應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="e3ebc-103">Creates an application gateway.</span></span>

## <span data-ttu-id="e3ebc-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3ebc-104">SYNTAX</span></span>

```
New-AzureApplicationGateway -Name <String> -VnetName <String>
 -Subnets <System.Collections.Generic.List`1[System.String]> [-InstanceCount <UInt32>] [-GatewaySize <String>]
 [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e3ebc-105">說明</span><span class="sxs-lookup"><span data-stu-id="e3ebc-105">DESCRIPTION</span></span>
<span data-ttu-id="e3ebc-106">**新的-AzureApplicationGateway** Cmdlet 會建立應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="e3ebc-106">The **New-AzureApplicationGateway** cmdlet creates an application gateway.</span></span>

## <span data-ttu-id="e3ebc-107">示例</span><span class="sxs-lookup"><span data-stu-id="e3ebc-107">EXAMPLES</span></span>

### <span data-ttu-id="e3ebc-108">範例1：建立應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="e3ebc-108">Example 1: Create an application gateway</span></span>
```
PS C:\> New-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork17" -Subnets @("Subnet01", "Subnet02", "Subnet03")
```

<span data-ttu-id="e3ebc-109">這個命令會建立名為 ApplicationGateway06 的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="e3ebc-109">This command creates an application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="e3ebc-110">此命令會在 VirtualNetwork17 和指定的子網中部署閘道。</span><span class="sxs-lookup"><span data-stu-id="e3ebc-110">The command deploys the gateway in VirtualNetwork17 and in the specified subnets.</span></span>

## <span data-ttu-id="e3ebc-111">參數</span><span class="sxs-lookup"><span data-stu-id="e3ebc-111">PARAMETERS</span></span>

### <span data-ttu-id="e3ebc-112">-描述</span><span class="sxs-lookup"><span data-stu-id="e3ebc-112">-Description</span></span>
<span data-ttu-id="e3ebc-113">指定此 Cmdlet 指派給應用程式閘道的描述。</span><span class="sxs-lookup"><span data-stu-id="e3ebc-113">Specifies a description that this cmdlet assigns to the application gateway.</span></span>

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

### <span data-ttu-id="e3ebc-114">-GatewaySize</span><span class="sxs-lookup"><span data-stu-id="e3ebc-114">-GatewaySize</span></span>
<span data-ttu-id="e3ebc-115">指定此 Cmdlet 指派給應用程式閘道的大小。</span><span class="sxs-lookup"><span data-stu-id="e3ebc-115">Specifies the size that this cmdlet assigns to the application gateway.</span></span>
<span data-ttu-id="e3ebc-116">有效值為：</span><span class="sxs-lookup"><span data-stu-id="e3ebc-116">Valid values are:</span></span>

- <span data-ttu-id="e3ebc-117">小規模</span><span class="sxs-lookup"><span data-stu-id="e3ebc-117">Small</span></span>
- <span data-ttu-id="e3ebc-118">深淺</span><span class="sxs-lookup"><span data-stu-id="e3ebc-118">Medium</span></span>
- <span data-ttu-id="e3ebc-119">大中型</span><span class="sxs-lookup"><span data-stu-id="e3ebc-119">Large</span></span>

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

### <span data-ttu-id="e3ebc-120">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="e3ebc-120">-InstanceCount</span></span>
<span data-ttu-id="e3ebc-121">指定此 Cmdlet 指派給應用程式閘道的實例數。</span><span class="sxs-lookup"><span data-stu-id="e3ebc-121">Specifies the number of instances that this cmdlet assigns to the application gateway.</span></span>

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

### <span data-ttu-id="e3ebc-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="e3ebc-122">-Name</span></span>
<span data-ttu-id="e3ebc-123">指定新應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3ebc-123">Specifies a name for the new application gateway.</span></span>

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

### <span data-ttu-id="e3ebc-124">-設定檔</span><span class="sxs-lookup"><span data-stu-id="e3ebc-124">-Profile</span></span>
<span data-ttu-id="e3ebc-125">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e3ebc-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e3ebc-126">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="e3ebc-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e3ebc-127">-子網</span><span class="sxs-lookup"><span data-stu-id="e3ebc-127">-Subnets</span></span>
<span data-ttu-id="e3ebc-128">指定此 Cmdlet 在其中部署應用程式閘道的子網陣列。</span><span class="sxs-lookup"><span data-stu-id="e3ebc-128">Specifies an array of subnets in which this cmdlet deploys the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3ebc-129">-VnetName</span><span class="sxs-lookup"><span data-stu-id="e3ebc-129">-VnetName</span></span>
<span data-ttu-id="e3ebc-130">指定此 Cmdlet 在哪個虛擬網路中部署應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="e3ebc-130">Specifies the virtual network in which this cmdlet deploys the application gateway.</span></span>

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

### <span data-ttu-id="e3ebc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3ebc-131">CommonParameters</span></span>
<span data-ttu-id="e3ebc-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3ebc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3ebc-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e3ebc-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3ebc-134">輸入</span><span class="sxs-lookup"><span data-stu-id="e3ebc-134">INPUTS</span></span>

### <span data-ttu-id="e3ebc-135">System.object</span><span class="sxs-lookup"><span data-stu-id="e3ebc-135">System.String</span></span>

## <span data-ttu-id="e3ebc-136">輸出</span><span class="sxs-lookup"><span data-stu-id="e3ebc-136">OUTPUTS</span></span>

### <span data-ttu-id="e3ebc-137">ApplicationGatewayOperationResponse 的 ApplicationGateway。 WindowsAzure</span><span class="sxs-lookup"><span data-stu-id="e3ebc-137">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="e3ebc-138">筆記</span><span class="sxs-lookup"><span data-stu-id="e3ebc-138">NOTES</span></span>

## <span data-ttu-id="e3ebc-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3ebc-139">RELATED LINKS</span></span>

[<span data-ttu-id="e3ebc-140">AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3ebc-140">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="e3ebc-141">移除-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3ebc-141">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="e3ebc-142">開始-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3ebc-142">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="e3ebc-143">停止 AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3ebc-143">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="e3ebc-144">更新-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3ebc-144">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)

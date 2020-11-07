---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D7D99AFA-A85E-43DA-9F2F-8FFD34048E00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ede675ab58905f102fb9d0029669115acdb9e85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967875"
---
# <span data-ttu-id="4131e-101">Set-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="4131e-101">Set-AzureApplicationGatewayConfig</span></span>

## <span data-ttu-id="4131e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4131e-102">SYNOPSIS</span></span>
<span data-ttu-id="4131e-103">設定應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4131e-103">Configures an application gateway.</span></span>

## <span data-ttu-id="4131e-104">句法</span><span class="sxs-lookup"><span data-stu-id="4131e-104">SYNTAX</span></span>

### <span data-ttu-id="4131e-105">Read-configfile</span><span class="sxs-lookup"><span data-stu-id="4131e-105">configFile</span></span>
```
Set-AzureApplicationGatewayConfig -Name <String> -ConfigFile <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="4131e-106">configObject</span><span class="sxs-lookup"><span data-stu-id="4131e-106">configObject</span></span>
```
Set-AzureApplicationGatewayConfig -Name <String> -Config <ApplicationGatewayConfiguration>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4131e-107">說明</span><span class="sxs-lookup"><span data-stu-id="4131e-107">DESCRIPTION</span></span>
<span data-ttu-id="4131e-108">AzureApplicationGatewayConfig Cmdlet 會 **設定** 應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4131e-108">The **Set-AzureApplicationGatewayConfig** cmdlet configures an application gateway.</span></span>

## <span data-ttu-id="4131e-109">示例</span><span class="sxs-lookup"><span data-stu-id="4131e-109">EXAMPLES</span></span>

### <span data-ttu-id="4131e-110">範例1：使用設定物件來設定應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="4131e-110">Example 1: Configure an application gateway by using a configuration object</span></span>
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway02"
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -Config $ConfigReturnObject
```

<span data-ttu-id="4131e-111">第一個命令會使用 **AzureApplicationGatewayConfig** Cmdlet，透過名為 ApplicationGateway02 的應用程式閘道取得 configuration 物件。</span><span class="sxs-lookup"><span data-stu-id="4131e-111">The first command gets the configuration object for the application gateway named ApplicationGateway02 by using the **Get-AzureApplicationGatewayConfig** cmdlet.</span></span>
<span data-ttu-id="4131e-112">該命令會將它儲存在 $ConfigReturnObject 變數中。</span><span class="sxs-lookup"><span data-stu-id="4131e-112">The command stores it in the $ConfigReturnObject variable.</span></span>

<span data-ttu-id="4131e-113">第二個命令會使用 $ConfigReturnObject 變數中所儲存的應用程式閘道設定物件，來設定名為 ApplicationGateway06 之應用程式的配置。</span><span class="sxs-lookup"><span data-stu-id="4131e-113">The second command sets the configuration for the application named ApplicationGateway06 by using an application gateway configuration object stored in the $ConfigReturnObject variable.</span></span>

### <span data-ttu-id="4131e-114">範例2：使用設定檔設定應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="4131e-114">Example 2: Configure an application gateway by using a configuration file</span></span>
```
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ConfigFile "D:\config.xml"
```

<span data-ttu-id="4131e-115">這個命令會在指定位置中使用應用程式閘道設定檔案，來設定名為 ApplicationGateway06 的應用程式的設定。</span><span class="sxs-lookup"><span data-stu-id="4131e-115">This command sets the configuration for the application named ApplicationGateway06 by using an application gateway configuration file in the specified location.</span></span>

### <span data-ttu-id="4131e-116">範例3：使用設定物件修改配置</span><span class="sxs-lookup"><span data-stu-id="4131e-116">Example 3: Modify a configuration by using a configuration object</span></span>
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
PS C:\> $ConfigReturnObject.Config.FrontendPorts[0].Port = 443
PS C:\> $ConfigReturnObject | Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
```

<span data-ttu-id="4131e-117">第一個命令會使用 **AzureApplicationGatewayConfig** Cmdlet，透過名為 ApplicationGateway06 的應用程式閘道取得 configuration 物件。</span><span class="sxs-lookup"><span data-stu-id="4131e-117">The first command gets the configuration object for the application gateway named ApplicationGateway06 by using the **Get-AzureApplicationGatewayConfig** cmdlet.</span></span>
<span data-ttu-id="4131e-118">該命令會將它儲存在 $ConfigReturnObject 變數中。</span><span class="sxs-lookup"><span data-stu-id="4131e-118">The command stores it in the $ConfigReturnObject variable.</span></span>

<span data-ttu-id="4131e-119">第二個命令會將埠值指派給儲存在 $ConfigReturnObject 的物件中的 **port** 屬性。</span><span class="sxs-lookup"><span data-stu-id="4131e-119">The second command assigns a port value to a **Port** property in the object stored in $ConfigReturnObject.</span></span>

<span data-ttu-id="4131e-120">最終命令會將更新的 $ConfigReturnObject 傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4131e-120">The final command passes the updated $ConfigReturnObject to the current cmdlet.</span></span>

## <span data-ttu-id="4131e-121">參數</span><span class="sxs-lookup"><span data-stu-id="4131e-121">PARAMETERS</span></span>

### <span data-ttu-id="4131e-122">-Config</span><span class="sxs-lookup"><span data-stu-id="4131e-122">-Config</span></span>
<span data-ttu-id="4131e-123">指定應用程式閘道設定物件。</span><span class="sxs-lookup"><span data-stu-id="4131e-123">Specifies an application gateway configuration object.</span></span>
<span data-ttu-id="4131e-124">這個 Cmdlet 會將此參數指定的設定指派給應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4131e-124">This cmdlet assigns the configuration that this parameter specifies to an application gateway.</span></span>

```yaml
Type: ApplicationGatewayConfiguration
Parameter Sets: configObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4131e-125">-Read-configfile</span><span class="sxs-lookup"><span data-stu-id="4131e-125">-ConfigFile</span></span>
<span data-ttu-id="4131e-126">以 XML 格式指定應用程式閘道的設定檔路徑。</span><span class="sxs-lookup"><span data-stu-id="4131e-126">Specifies the path of a configuration file, in XML format, for an application gateway.</span></span>
<span data-ttu-id="4131e-127">這個 Cmdlet 會將此參數指定的設定指派給應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4131e-127">This cmdlet assigns the configuration that this parameter specifies to an application gateway.</span></span>

```yaml
Type: String
Parameter Sets: configFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4131e-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="4131e-128">-Name</span></span>
<span data-ttu-id="4131e-129">指定此 Cmdlet 所設定之應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="4131e-129">Specifies the name of the application gateway that this cmdlet configures.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4131e-130">-設定檔</span><span class="sxs-lookup"><span data-stu-id="4131e-130">-Profile</span></span>
<span data-ttu-id="4131e-131">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="4131e-131">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="4131e-132">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="4131e-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4131e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4131e-133">CommonParameters</span></span>
<span data-ttu-id="4131e-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4131e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4131e-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4131e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4131e-136">輸入</span><span class="sxs-lookup"><span data-stu-id="4131e-136">INPUTS</span></span>

### <span data-ttu-id="4131e-137">ApplicationGatewayObjectModel. ApplicationGatewayConfiguration （系統字串）</span><span class="sxs-lookup"><span data-stu-id="4131e-137">System.String, Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayConfiguration</span></span>

## <span data-ttu-id="4131e-138">輸出</span><span class="sxs-lookup"><span data-stu-id="4131e-138">OUTPUTS</span></span>

### <span data-ttu-id="4131e-139">ApplicationGatewayOperationResponse 的 ApplicationGateway。 WindowsAzure</span><span class="sxs-lookup"><span data-stu-id="4131e-139">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="4131e-140">筆記</span><span class="sxs-lookup"><span data-stu-id="4131e-140">NOTES</span></span>

## <span data-ttu-id="4131e-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="4131e-141">RELATED LINKS</span></span>

[<span data-ttu-id="4131e-142">AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="4131e-142">Get-AzureApplicationGatewayConfig</span></span>](./Get-AzureApplicationGatewayConfig.md)



---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A2F0ECAD-595C-45E6-98AC-2C7DB8E4BEF0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4dac85bf4c8b3d0a0f0f4b27cd249a98e020be7d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967111"
---
# <span data-ttu-id="889c1-101">Get-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="889c1-101">Get-AzureApplicationGatewayConfig</span></span>

## <span data-ttu-id="889c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="889c1-102">SYNOPSIS</span></span>
<span data-ttu-id="889c1-103">取得應用程式閘道配置內容。</span><span class="sxs-lookup"><span data-stu-id="889c1-103">Gets an Application Gateway configuration context.</span></span>

## <span data-ttu-id="889c1-104">句法</span><span class="sxs-lookup"><span data-stu-id="889c1-104">SYNTAX</span></span>

```
Get-AzureApplicationGatewayConfig -Name <String> [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="889c1-105">說明</span><span class="sxs-lookup"><span data-stu-id="889c1-105">DESCRIPTION</span></span>
<span data-ttu-id="889c1-106">**AzureApplicationGatewayConfig** Cmdlet 會取得 Azure 應用程式閘道配置內容。</span><span class="sxs-lookup"><span data-stu-id="889c1-106">The **Get-AzureApplicationGatewayConfig** cmdlet gets an Azure Application Gateway configuration context.</span></span>
<span data-ttu-id="889c1-107">內容包括設定物件和 XML 配置。</span><span class="sxs-lookup"><span data-stu-id="889c1-107">A context includes both a configuration object and XML configuration.</span></span>
<span data-ttu-id="889c1-108">您可以將 XML 配置儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="889c1-108">You can save the XML configuration to a file.</span></span>

## <span data-ttu-id="889c1-109">示例</span><span class="sxs-lookup"><span data-stu-id="889c1-109">EXAMPLES</span></span>

### <span data-ttu-id="889c1-110">範例1：取得應用程式閘道設定並將它儲存至檔案</span><span class="sxs-lookup"><span data-stu-id="889c1-110">Example 1: Get an Application Gateway configuration and save it to a file</span></span>
```
PS C:\> Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ExportToFile "D:\config.xml"
```

<span data-ttu-id="889c1-111">這個命令會取得名為 ApplicationGateway06 的應用程式閘道的配置。</span><span class="sxs-lookup"><span data-stu-id="889c1-111">This command gets the configuration for an Application Gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="889c1-112">該命令會將它儲存在檔案中指定的路徑。</span><span class="sxs-lookup"><span data-stu-id="889c1-112">The command saves it in the file in the specified path.</span></span>

## <span data-ttu-id="889c1-113">參數</span><span class="sxs-lookup"><span data-stu-id="889c1-113">PARAMETERS</span></span>

### <span data-ttu-id="889c1-114">-ExportToFile</span><span class="sxs-lookup"><span data-stu-id="889c1-114">-ExportToFile</span></span>
<span data-ttu-id="889c1-115">指定此 Cmdlet 以 XML 格式儲存配置的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="889c1-115">Specifies a file path to which this cmdlet saves the configuration in XML format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="889c1-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="889c1-116">-Name</span></span>
<span data-ttu-id="889c1-117">指定此 Cmdlet 取得配置資訊之應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="889c1-117">Specifies the name of the Application Gateway for which this cmdlet gets configuration information.</span></span>

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

### <span data-ttu-id="889c1-118">-設定檔</span><span class="sxs-lookup"><span data-stu-id="889c1-118">-Profile</span></span>
<span data-ttu-id="889c1-119">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="889c1-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="889c1-120">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="889c1-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="889c1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="889c1-121">CommonParameters</span></span>
<span data-ttu-id="889c1-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="889c1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="889c1-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="889c1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="889c1-124">輸入</span><span class="sxs-lookup"><span data-stu-id="889c1-124">INPUTS</span></span>

### <span data-ttu-id="889c1-125">System.object</span><span class="sxs-lookup"><span data-stu-id="889c1-125">System.String</span></span>

## <span data-ttu-id="889c1-126">輸出</span><span class="sxs-lookup"><span data-stu-id="889c1-126">OUTPUTS</span></span>

### <span data-ttu-id="889c1-127">ApplicationGatewayObjectModel.. ApplicationGatewayConfigCoNtext</span><span class="sxs-lookup"><span data-stu-id="889c1-127">Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayConfigContext</span></span>

## <span data-ttu-id="889c1-128">筆記</span><span class="sxs-lookup"><span data-stu-id="889c1-128">NOTES</span></span>

## <span data-ttu-id="889c1-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="889c1-129">RELATED LINKS</span></span>

[<span data-ttu-id="889c1-130">Set-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="889c1-130">Set-AzureApplicationGatewayConfig</span></span>](./Set-AzureApplicationGatewayConfig.md)



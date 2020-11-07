---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 0AED21E8-A638-4019-9B23-447472E56C7A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 202066cfc2649b0f56810123e211bbeb5d69720f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967116"
---
# <span data-ttu-id="1083f-101">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1083f-101">Get-AzureApplicationGateway</span></span>

## <span data-ttu-id="1083f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1083f-102">SYNOPSIS</span></span>
<span data-ttu-id="1083f-103">取得應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="1083f-103">Gets an Application Gateway.</span></span>

## <span data-ttu-id="1083f-104">句法</span><span class="sxs-lookup"><span data-stu-id="1083f-104">SYNTAX</span></span>

```
Get-AzureApplicationGateway [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1083f-105">說明</span><span class="sxs-lookup"><span data-stu-id="1083f-105">DESCRIPTION</span></span>
<span data-ttu-id="1083f-106">**AzureApplicationGateway** Cmdlet 會取得現有的 Azure 應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="1083f-106">The **Get-AzureApplicationGateway** cmdlet gets an existing Azure Application Gateway.</span></span>

## <span data-ttu-id="1083f-107">示例</span><span class="sxs-lookup"><span data-stu-id="1083f-107">EXAMPLES</span></span>

### <span data-ttu-id="1083f-108">範例1：取得應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="1083f-108">Example 1: Get an Application Gateway</span></span>
```
PS C:\> Get-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="1083f-109">這個命令會取得名為 ApplicationGateway06 的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="1083f-109">This command gets the Application Gateway named ApplicationGateway06.</span></span>

### <span data-ttu-id="1083f-110">範例2：取得所有應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="1083f-110">Example 2: Get all Application Gateways</span></span>
```
PS C:\> Get-AzureApplicationGateway
```

<span data-ttu-id="1083f-111">這個命令會在您的訂閱下取得所有的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="1083f-111">This command gets all the Application Gateways under your subscription.</span></span>

## <span data-ttu-id="1083f-112">參數</span><span class="sxs-lookup"><span data-stu-id="1083f-112">PARAMETERS</span></span>

### <span data-ttu-id="1083f-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="1083f-113">-Name</span></span>
<span data-ttu-id="1083f-114">指定此 Cmdlet 所取得之應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="1083f-114">Specifies the name of the Application Gateway that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1083f-115">-設定檔</span><span class="sxs-lookup"><span data-stu-id="1083f-115">-Profile</span></span>
<span data-ttu-id="1083f-116">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="1083f-116">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="1083f-117">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="1083f-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1083f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1083f-118">CommonParameters</span></span>
<span data-ttu-id="1083f-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1083f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1083f-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1083f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1083f-121">輸入</span><span class="sxs-lookup"><span data-stu-id="1083f-121">INPUTS</span></span>

### <span data-ttu-id="1083f-122">System.object</span><span class="sxs-lookup"><span data-stu-id="1083f-122">System.String</span></span>

## <span data-ttu-id="1083f-123">輸出</span><span class="sxs-lookup"><span data-stu-id="1083f-123">OUTPUTS</span></span>

### <span data-ttu-id="1083f-124">ApplicationGatewayObjectModel ApplicationGateway，IEnumerable. ApplicationGateway<ApplicationGatewayObjectModel..></span><span class="sxs-lookup"><span data-stu-id="1083f-124">Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGateway, IEnumerable<Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGateway></span></span>

## <span data-ttu-id="1083f-125">筆記</span><span class="sxs-lookup"><span data-stu-id="1083f-125">NOTES</span></span>

## <span data-ttu-id="1083f-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="1083f-126">RELATED LINKS</span></span>

[<span data-ttu-id="1083f-127">新-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1083f-127">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="1083f-128">移除-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1083f-128">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="1083f-129">開始-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1083f-129">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="1083f-130">停止 AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1083f-130">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="1083f-131">更新-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1083f-131">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)



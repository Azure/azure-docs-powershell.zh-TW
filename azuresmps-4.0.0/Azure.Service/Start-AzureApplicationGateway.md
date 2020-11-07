---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D50984B7-FD97-4713-8E56-1C06D2B008E3
online version: ''
schema: 2.0.0
ms.openlocfilehash: a01d59d6a0755b3763eaef9b7532326ca0ffd402
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967225"
---
# <span data-ttu-id="2e8fb-101">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2e8fb-101">Start-AzureApplicationGateway</span></span>

## <span data-ttu-id="2e8fb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2e8fb-102">SYNOPSIS</span></span>
<span data-ttu-id="2e8fb-103">啟動應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="2e8fb-103">Starts an application gateway.</span></span>

## <span data-ttu-id="2e8fb-104">句法</span><span class="sxs-lookup"><span data-stu-id="2e8fb-104">SYNTAX</span></span>

```
Start-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2e8fb-105">說明</span><span class="sxs-lookup"><span data-stu-id="2e8fb-105">DESCRIPTION</span></span>
<span data-ttu-id="2e8fb-106">**Start AzureApplicationGateway** Cmdlet 會啟動應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="2e8fb-106">The **Start-AzureApplicationGateway** cmdlet starts an application gateway.</span></span>

## <span data-ttu-id="2e8fb-107">示例</span><span class="sxs-lookup"><span data-stu-id="2e8fb-107">EXAMPLES</span></span>

### <span data-ttu-id="2e8fb-108">範例1：啟動應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="2e8fb-108">Example 1: Start an application gateway</span></span>
```
PS C:\> Start-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="2e8fb-109">這個命令會啟動名為 ApplicationGateway06 的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="2e8fb-109">This command starts the application gateway named ApplicationGateway06.</span></span>

## <span data-ttu-id="2e8fb-110">參數</span><span class="sxs-lookup"><span data-stu-id="2e8fb-110">PARAMETERS</span></span>

### <span data-ttu-id="2e8fb-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="2e8fb-111">-Name</span></span>
<span data-ttu-id="2e8fb-112">指定此 Cmdlet 啟動之應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="2e8fb-112">Specifies the name of the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="2e8fb-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="2e8fb-113">-Profile</span></span>
<span data-ttu-id="2e8fb-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="2e8fb-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="2e8fb-115">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="2e8fb-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2e8fb-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e8fb-116">CommonParameters</span></span>
<span data-ttu-id="2e8fb-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2e8fb-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e8fb-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2e8fb-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e8fb-119">輸入</span><span class="sxs-lookup"><span data-stu-id="2e8fb-119">INPUTS</span></span>

### <span data-ttu-id="2e8fb-120">System.object</span><span class="sxs-lookup"><span data-stu-id="2e8fb-120">System.String</span></span>

## <span data-ttu-id="2e8fb-121">輸出</span><span class="sxs-lookup"><span data-stu-id="2e8fb-121">OUTPUTS</span></span>

### <span data-ttu-id="2e8fb-122">ApplicationGatewayOperationResponse 的 ApplicationGateway。 WindowsAzure</span><span class="sxs-lookup"><span data-stu-id="2e8fb-122">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="2e8fb-123">筆記</span><span class="sxs-lookup"><span data-stu-id="2e8fb-123">NOTES</span></span>

## <span data-ttu-id="2e8fb-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="2e8fb-124">RELATED LINKS</span></span>

[<span data-ttu-id="2e8fb-125">AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2e8fb-125">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="2e8fb-126">新-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2e8fb-126">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="2e8fb-127">移除-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2e8fb-127">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="2e8fb-128">停止 AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2e8fb-128">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="2e8fb-129">更新-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2e8fb-129">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)



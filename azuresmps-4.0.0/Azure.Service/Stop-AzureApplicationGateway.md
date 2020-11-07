---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 17BA2ED5-E347-45C0-AF20-CDD288469514
online version: ''
schema: 2.0.0
ms.openlocfilehash: a07afcadb2207f2e4377601abfa6094bc3293328
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967854"
---
# <span data-ttu-id="b087a-101">Stop-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b087a-101">Stop-AzureApplicationGateway</span></span>

## <span data-ttu-id="b087a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b087a-102">SYNOPSIS</span></span>
<span data-ttu-id="b087a-103">停止應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="b087a-103">Stops an application gateway.</span></span>

## <span data-ttu-id="b087a-104">句法</span><span class="sxs-lookup"><span data-stu-id="b087a-104">SYNTAX</span></span>

```
Stop-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b087a-105">說明</span><span class="sxs-lookup"><span data-stu-id="b087a-105">DESCRIPTION</span></span>
<span data-ttu-id="b087a-106">**AzureApplicationGateway** Cmdlet 會停止應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="b087a-106">The **Stop-AzureApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="b087a-107">示例</span><span class="sxs-lookup"><span data-stu-id="b087a-107">EXAMPLES</span></span>

### <span data-ttu-id="b087a-108">範例1：停止應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="b087a-108">Example 1: Stop an application gateway</span></span>
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="b087a-109">這個命令會停止名為 ApplicationGateway06 的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="b087a-109">This command stops the application gateway named ApplicationGateway06.</span></span>

## <span data-ttu-id="b087a-110">參數</span><span class="sxs-lookup"><span data-stu-id="b087a-110">PARAMETERS</span></span>

### <span data-ttu-id="b087a-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="b087a-111">-Name</span></span>
<span data-ttu-id="b087a-112">指定此 Cmdlet 停止的應用程式閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="b087a-112">Specifies the name of the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="b087a-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="b087a-113">-Profile</span></span>
<span data-ttu-id="b087a-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b087a-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b087a-115">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="b087a-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b087a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b087a-116">CommonParameters</span></span>
<span data-ttu-id="b087a-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b087a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b087a-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b087a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b087a-119">輸入</span><span class="sxs-lookup"><span data-stu-id="b087a-119">INPUTS</span></span>

### <span data-ttu-id="b087a-120">System.object</span><span class="sxs-lookup"><span data-stu-id="b087a-120">System.String</span></span>

## <span data-ttu-id="b087a-121">輸出</span><span class="sxs-lookup"><span data-stu-id="b087a-121">OUTPUTS</span></span>

### <span data-ttu-id="b087a-122">ApplicationGatewayOperationResponse 的 ApplicationGateway。 WindowsAzure</span><span class="sxs-lookup"><span data-stu-id="b087a-122">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="b087a-123">筆記</span><span class="sxs-lookup"><span data-stu-id="b087a-123">NOTES</span></span>

## <span data-ttu-id="b087a-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="b087a-124">RELATED LINKS</span></span>

[<span data-ttu-id="b087a-125">AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b087a-125">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="b087a-126">新-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b087a-126">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="b087a-127">移除-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b087a-127">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="b087a-128">開始-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b087a-128">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="b087a-129">更新-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b087a-129">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)

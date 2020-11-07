---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 128AD64D-709A-4B59-B233-4221A9120AE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4803fd24952066c4dcea72daaf0c999b64ae4c5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967943"
---
# <span data-ttu-id="3be90-101">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3be90-101">Remove-AzureApplicationGateway</span></span>

## <span data-ttu-id="3be90-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3be90-102">SYNOPSIS</span></span>
<span data-ttu-id="3be90-103">移除應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="3be90-103">Removes an application gateway.</span></span>

## <span data-ttu-id="3be90-104">句法</span><span class="sxs-lookup"><span data-stu-id="3be90-104">SYNTAX</span></span>

```
Remove-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3be90-105">說明</span><span class="sxs-lookup"><span data-stu-id="3be90-105">DESCRIPTION</span></span>
<span data-ttu-id="3be90-106">**AzureApplicationGateway** Cmdlet 會移除應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="3be90-106">The **Remove-AzureApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="3be90-107">示例</span><span class="sxs-lookup"><span data-stu-id="3be90-107">EXAMPLES</span></span>

### <span data-ttu-id="3be90-108">範例1：移除應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="3be90-108">Example 1: Remove an application gateway</span></span>
```
PS C:\> Remove-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="3be90-109">這個命令會移除名為 ApplicationGateway06 的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="3be90-109">This command removes the application gateway named ApplicationGateway06.</span></span>

## <span data-ttu-id="3be90-110">參數</span><span class="sxs-lookup"><span data-stu-id="3be90-110">PARAMETERS</span></span>

### <span data-ttu-id="3be90-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="3be90-111">-Name</span></span>
<span data-ttu-id="3be90-112">指定此 Cmdlet 移除之應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="3be90-112">Specifies the name of the application gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3be90-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="3be90-113">-Profile</span></span>
<span data-ttu-id="3be90-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="3be90-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3be90-115">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="3be90-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3be90-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3be90-116">CommonParameters</span></span>
<span data-ttu-id="3be90-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3be90-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3be90-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3be90-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3be90-119">輸入</span><span class="sxs-lookup"><span data-stu-id="3be90-119">INPUTS</span></span>

### <span data-ttu-id="3be90-120">System.object</span><span class="sxs-lookup"><span data-stu-id="3be90-120">System.String</span></span>

## <span data-ttu-id="3be90-121">輸出</span><span class="sxs-lookup"><span data-stu-id="3be90-121">OUTPUTS</span></span>

### <span data-ttu-id="3be90-122">ApplicationGatewayOperationResponse 的 ApplicationGateway。 WindowsAzure</span><span class="sxs-lookup"><span data-stu-id="3be90-122">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="3be90-123">筆記</span><span class="sxs-lookup"><span data-stu-id="3be90-123">NOTES</span></span>

## <span data-ttu-id="3be90-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="3be90-124">RELATED LINKS</span></span>

[<span data-ttu-id="3be90-125">AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3be90-125">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="3be90-126">新-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3be90-126">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="3be90-127">開始-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3be90-127">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="3be90-128">停止 AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3be90-128">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="3be90-129">更新-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3be90-129">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)



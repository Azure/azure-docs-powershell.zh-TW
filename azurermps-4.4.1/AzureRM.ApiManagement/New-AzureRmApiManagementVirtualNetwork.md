---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: 42213ddd4a7780b4d69b357c4b801df34aa9aca4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445212"
---
# <span data-ttu-id="a29c9-101">New-AzureRmApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a29c9-101">New-AzureRmApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="a29c9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a29c9-102">SYNOPSIS</span></span>
<span data-ttu-id="a29c9-103">建立 PsApiManagementVirtualNetwork 的實例。</span><span class="sxs-lookup"><span data-stu-id="a29c9-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a29c9-104">句法</span><span class="sxs-lookup"><span data-stu-id="a29c9-104">SYNTAX</span></span>

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a29c9-105">說明</span><span class="sxs-lookup"><span data-stu-id="a29c9-105">DESCRIPTION</span></span>
<span data-ttu-id="a29c9-106">**新的-AzureRmApiManagementVirtualNetwork** Cmdlet 是協助程式命令，可建立 **PsApiManagementVirtualNetwork** 的實例。</span><span class="sxs-lookup"><span data-stu-id="a29c9-106">The **New-AzureRmApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="a29c9-107">此命令與 **AzureRMApiManagementVirtualNetworks** Cmdlet 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="a29c9-107">This command is used with **Set-AzureRMApiManagementVirtualNetworks** cmdlet.</span></span>

## <span data-ttu-id="a29c9-108">示例</span><span class="sxs-lookup"><span data-stu-id="a29c9-108">EXAMPLES</span></span>

### <span data-ttu-id="a29c9-109">範例1：建立虛擬網路</span><span class="sxs-lookup"><span data-stu-id="a29c9-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$VirtualNetworks = @()
PS C:\> $VirtualNetworks += New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubtenName "ContosoNet" -VnetId "089D3F4D-B986-4DFD-9259-9112BA7A1F03"
PS C:\> Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $VirtualNetworks
```

<span data-ttu-id="a29c9-110">這個範例會建立一個虛擬網路，然後呼叫 **AzureRmApiManagementVirtualNetworks** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a29c9-110">This example creates a virtual network and then calls the **Set-AzureRmApiManagementVirtualNetworks** cmdlet.</span></span>

## <span data-ttu-id="a29c9-111">參數</span><span class="sxs-lookup"><span data-stu-id="a29c9-111">PARAMETERS</span></span>

### <span data-ttu-id="a29c9-112">-位置</span><span class="sxs-lookup"><span data-stu-id="a29c9-112">-Location</span></span>
<span data-ttu-id="a29c9-113">指定此 Cmdlet 建立實例之虛擬網路的位置。</span><span class="sxs-lookup"><span data-stu-id="a29c9-113">Specifies the location of the virtual network in which this cmdlet creates the instance.</span></span>

<span data-ttu-id="a29c9-114">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a29c9-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a29c9-115">美國中北部</span><span class="sxs-lookup"><span data-stu-id="a29c9-115">North Central US</span></span>
- <span data-ttu-id="a29c9-116">美國中南部</span><span class="sxs-lookup"><span data-stu-id="a29c9-116">South Central US</span></span>
- <span data-ttu-id="a29c9-117">美國中部</span><span class="sxs-lookup"><span data-stu-id="a29c9-117">Central US</span></span>
- <span data-ttu-id="a29c9-118">西歐</span><span class="sxs-lookup"><span data-stu-id="a29c9-118">West Europe</span></span>
- <span data-ttu-id="a29c9-119">北歐</span><span class="sxs-lookup"><span data-stu-id="a29c9-119">North Europe</span></span>
- <span data-ttu-id="a29c9-120">美國西部</span><span class="sxs-lookup"><span data-stu-id="a29c9-120">West US</span></span>
- <span data-ttu-id="a29c9-121">東美國</span><span class="sxs-lookup"><span data-stu-id="a29c9-121">East US</span></span>
- <span data-ttu-id="a29c9-122">東美國2</span><span class="sxs-lookup"><span data-stu-id="a29c9-122">East US 2</span></span>
- <span data-ttu-id="a29c9-123">日本東</span><span class="sxs-lookup"><span data-stu-id="a29c9-123">Japan East</span></span>
- <span data-ttu-id="a29c9-124">日本西部</span><span class="sxs-lookup"><span data-stu-id="a29c9-124">Japan West</span></span>
- <span data-ttu-id="a29c9-125">巴西南部</span><span class="sxs-lookup"><span data-stu-id="a29c9-125">Brazil South</span></span>
- <span data-ttu-id="a29c9-126">東南亞</span><span class="sxs-lookup"><span data-stu-id="a29c9-126">Southeast Asia</span></span>
- <span data-ttu-id="a29c9-127">東亞</span><span class="sxs-lookup"><span data-stu-id="a29c9-127">East Asia</span></span>
- <span data-ttu-id="a29c9-128">澳大利亞東</span><span class="sxs-lookup"><span data-stu-id="a29c9-128">Australia East</span></span>
- <span data-ttu-id="a29c9-129">澳大利亞東南部</span><span class="sxs-lookup"><span data-stu-id="a29c9-129">Australia Southeast</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a29c9-130">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="a29c9-130">-SubnetResourceId</span></span>
<span data-ttu-id="a29c9-131">指定虛擬網路的子網資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a29c9-131">Specifies the subnet resource ID of the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a29c9-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a29c9-132">-DefaultProfile</span></span>
<span data-ttu-id="a29c9-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a29c9-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a29c9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a29c9-134">CommonParameters</span></span>
<span data-ttu-id="a29c9-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a29c9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a29c9-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a29c9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a29c9-137">輸入</span><span class="sxs-lookup"><span data-stu-id="a29c9-137">INPUTS</span></span>

## <span data-ttu-id="a29c9-138">輸出</span><span class="sxs-lookup"><span data-stu-id="a29c9-138">OUTPUTS</span></span>

### <span data-ttu-id="a29c9-139">PsApiManagementVirtualNetwork 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="a29c9-139">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="a29c9-140">筆記</span><span class="sxs-lookup"><span data-stu-id="a29c9-140">NOTES</span></span>

## <span data-ttu-id="a29c9-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="a29c9-141">RELATED LINKS</span></span>


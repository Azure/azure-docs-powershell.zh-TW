---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMPlan.md
ms.openlocfilehash: c6c17978840fd5c446d7d89350f1792091a5cffa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623604"
---
# <span data-ttu-id="0dc82-101">Set-AzureRmVMPlan</span><span class="sxs-lookup"><span data-stu-id="0dc82-101">Set-AzureRmVMPlan</span></span>

## <span data-ttu-id="0dc82-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0dc82-102">SYNOPSIS</span></span>
<span data-ttu-id="0dc82-103">在虛擬機器上設定 Marketplace 方案資訊。</span><span class="sxs-lookup"><span data-stu-id="0dc82-103">Sets the Marketplace plan information on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0dc82-104">句法</span><span class="sxs-lookup"><span data-stu-id="0dc82-104">SYNTAX</span></span>

```
Set-AzureRmVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [<CommonParameters>]
```

## <span data-ttu-id="0dc82-105">說明</span><span class="sxs-lookup"><span data-stu-id="0dc82-105">DESCRIPTION</span></span>
<span data-ttu-id="0dc82-106">**AzureRmVMPlan** Cmdlet 設定虛擬機器的 Azure Marketplace 方案資訊。</span><span class="sxs-lookup"><span data-stu-id="0dc82-106">The **Set-AzureRmVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>

<span data-ttu-id="0dc82-107">在能透過命令列部署 Marketplace 影像之前，必須啟用程式設計存取，或者必須使用 Azure 入口網站部署虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="0dc82-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="0dc82-108">示例</span><span class="sxs-lookup"><span data-stu-id="0dc82-108">EXAMPLES</span></span>

## <span data-ttu-id="0dc82-109">參數</span><span class="sxs-lookup"><span data-stu-id="0dc82-109">PARAMETERS</span></span>

### <span data-ttu-id="0dc82-110">-名稱</span><span class="sxs-lookup"><span data-stu-id="0dc82-110">-Name</span></span>
<span data-ttu-id="0dc82-111">指定 Marketplace 的影像名稱。</span><span class="sxs-lookup"><span data-stu-id="0dc82-111">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="0dc82-112">這與 Get-AzureRmVMImageSku Cmdlet 傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="0dc82-112">This is the same value that is returned by the Get-AzureRmVMImageSku cmdlet.</span></span>
<span data-ttu-id="0dc82-113">如需如何尋找影像資訊的詳細資訊，請參閱在 Microsoft Azure 檔中 [流覽並選取 Azure 虛擬機器影像與 PowerShell 以及 AZURE CLI](https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) 。</span><span class="sxs-lookup"><span data-stu-id="0dc82-113">For more information about how to find image information, see [Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLI](https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

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

### <span data-ttu-id="0dc82-114">-產品</span><span class="sxs-lookup"><span data-stu-id="0dc82-114">-Product</span></span>
<span data-ttu-id="0dc82-115">從 Marketplace 指定影像的產品。</span><span class="sxs-lookup"><span data-stu-id="0dc82-115">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="0dc82-116">此資訊與 **imageReference** 元素的 **提供** 值相同。</span><span class="sxs-lookup"><span data-stu-id="0dc82-116">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc82-117">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="0dc82-117">-PromotionCode</span></span>
<span data-ttu-id="0dc82-118">指定促銷代碼。</span><span class="sxs-lookup"><span data-stu-id="0dc82-118">Specifies a promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc82-119">-Publisher</span><span class="sxs-lookup"><span data-stu-id="0dc82-119">-Publisher</span></span>
<span data-ttu-id="0dc82-120">指定影像的發行者。</span><span class="sxs-lookup"><span data-stu-id="0dc82-120">Specifies the publisher of the image.</span></span>
<span data-ttu-id="0dc82-121">您可以使用 Get-AzureRmVMImagePublisher Cmdlet 來尋找此資訊。</span><span class="sxs-lookup"><span data-stu-id="0dc82-121">You can find this information by using the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc82-122">-VM</span><span class="sxs-lookup"><span data-stu-id="0dc82-122">-VM</span></span>
<span data-ttu-id="0dc82-123">指定要設定其 Marketplace 方案的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="0dc82-123">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="0dc82-124">您可以使用 Get-AzureRmVM Cmdlet 來取得虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="0dc82-124">You can use the Get-AzureRmVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="0dc82-125">您可以使用 New-AzureRmVMConfig Cmdlet 來建立虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="0dc82-125">You can use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc82-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dc82-126">CommonParameters</span></span>
<span data-ttu-id="0dc82-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0dc82-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dc82-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0dc82-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dc82-129">輸入</span><span class="sxs-lookup"><span data-stu-id="0dc82-129">INPUTS</span></span>

### <span data-ttu-id="0dc82-130">所有</span><span class="sxs-lookup"><span data-stu-id="0dc82-130">None</span></span>
<span data-ttu-id="0dc82-131">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="0dc82-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0dc82-132">輸出</span><span class="sxs-lookup"><span data-stu-id="0dc82-132">OUTPUTS</span></span>

## <span data-ttu-id="0dc82-133">筆記</span><span class="sxs-lookup"><span data-stu-id="0dc82-133">NOTES</span></span>

## <span data-ttu-id="0dc82-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="0dc82-134">RELATED LINKS</span></span>

[<span data-ttu-id="0dc82-135">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0dc82-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="0dc82-136">AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="0dc82-136">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="0dc82-137">AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="0dc82-137">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="0dc82-138">新-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="0dc82-138">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

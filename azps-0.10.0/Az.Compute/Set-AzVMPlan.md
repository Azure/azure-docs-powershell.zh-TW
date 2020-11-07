---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMPlan.md
ms.openlocfilehash: 63c23712373cd597766faff8fd57f7f4b38deaa1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795854"
---
# <span data-ttu-id="f08e3-101">Set-AzVMPlan</span><span class="sxs-lookup"><span data-stu-id="f08e3-101">Set-AzVMPlan</span></span>

## <span data-ttu-id="f08e3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f08e3-102">SYNOPSIS</span></span>
<span data-ttu-id="f08e3-103">在虛擬機器上設定 Marketplace 方案資訊。</span><span class="sxs-lookup"><span data-stu-id="f08e3-103">Sets the Marketplace plan information on a virtual machine.</span></span>

## <span data-ttu-id="f08e3-104">句法</span><span class="sxs-lookup"><span data-stu-id="f08e3-104">SYNTAX</span></span>

```
Set-AzVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f08e3-105">說明</span><span class="sxs-lookup"><span data-stu-id="f08e3-105">DESCRIPTION</span></span>
<span data-ttu-id="f08e3-106">**AzVMPlan** Cmdlet 設定虛擬機器的 Azure Marketplace 方案資訊。</span><span class="sxs-lookup"><span data-stu-id="f08e3-106">The **Set-AzVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>

<span data-ttu-id="f08e3-107">在能透過命令列部署 Marketplace 影像之前，必須啟用程式設計存取，或者必須使用 Azure 入口網站部署虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f08e3-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="f08e3-108">示例</span><span class="sxs-lookup"><span data-stu-id="f08e3-108">EXAMPLES</span></span>

## <span data-ttu-id="f08e3-109">參數</span><span class="sxs-lookup"><span data-stu-id="f08e3-109">PARAMETERS</span></span>

### <span data-ttu-id="f08e3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f08e3-110">-DefaultProfile</span></span>
<span data-ttu-id="f08e3-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f08e3-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f08e3-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="f08e3-112">-Name</span></span>
<span data-ttu-id="f08e3-113">指定 Marketplace 的影像名稱。</span><span class="sxs-lookup"><span data-stu-id="f08e3-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="f08e3-114">這與 Get-AzVMImageSku Cmdlet 傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="f08e3-114">This is the same value that is returned by the Get-AzVMImageSku cmdlet.</span></span>
<span data-ttu-id="f08e3-115">如需如何尋找影像資訊的詳細資訊，請參閱使用 PowerShell 流覽及選取 Azure 虛擬機器影像，以及 https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) Microsoft azure 檔中的 azure CLI (。</span><span class="sxs-lookup"><span data-stu-id="f08e3-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

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

### <span data-ttu-id="f08e3-116">-產品</span><span class="sxs-lookup"><span data-stu-id="f08e3-116">-Product</span></span>
<span data-ttu-id="f08e3-117">從 Marketplace 指定影像的產品。</span><span class="sxs-lookup"><span data-stu-id="f08e3-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="f08e3-118">此資訊與 **imageReference** 元素的 **提供** 值相同。</span><span class="sxs-lookup"><span data-stu-id="f08e3-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

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

### <span data-ttu-id="f08e3-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="f08e3-119">-PromotionCode</span></span>
<span data-ttu-id="f08e3-120">指定促銷代碼。</span><span class="sxs-lookup"><span data-stu-id="f08e3-120">Specifies a promotion code.</span></span>

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

### <span data-ttu-id="f08e3-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="f08e3-121">-Publisher</span></span>
<span data-ttu-id="f08e3-122">指定影像的發行者。</span><span class="sxs-lookup"><span data-stu-id="f08e3-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="f08e3-123">您可以使用 Get-AzVMImagePublisher Cmdlet 來尋找此資訊。</span><span class="sxs-lookup"><span data-stu-id="f08e3-123">You can find this information by using the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="f08e3-124">-VM</span><span class="sxs-lookup"><span data-stu-id="f08e3-124">-VM</span></span>
<span data-ttu-id="f08e3-125">指定要設定其 Marketplace 方案的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="f08e3-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="f08e3-126">您可以使用 Get-AzVM Cmdlet 來取得虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="f08e3-126">You can use the Get-AzVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="f08e3-127">您可以使用 New-AzVMConfig Cmdlet 來建立虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="f08e3-127">You can use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="f08e3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f08e3-128">CommonParameters</span></span>
<span data-ttu-id="f08e3-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f08e3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f08e3-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f08e3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f08e3-131">輸入</span><span class="sxs-lookup"><span data-stu-id="f08e3-131">INPUTS</span></span>

### <span data-ttu-id="f08e3-132">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f08e3-132">PSVirtualMachine</span></span>
<span data-ttu-id="f08e3-133">[VM "參數從管線接受類型 ' PSVirtualMachine」的值</span><span class="sxs-lookup"><span data-stu-id="f08e3-133">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="f08e3-134">輸出</span><span class="sxs-lookup"><span data-stu-id="f08e3-134">OUTPUTS</span></span>

### <span data-ttu-id="f08e3-135">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="f08e3-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="f08e3-136">筆記</span><span class="sxs-lookup"><span data-stu-id="f08e3-136">NOTES</span></span>

## <span data-ttu-id="f08e3-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="f08e3-137">RELATED LINKS</span></span>

[<span data-ttu-id="f08e3-138">AzVM</span><span class="sxs-lookup"><span data-stu-id="f08e3-138">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="f08e3-139">AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="f08e3-139">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="f08e3-140">AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="f08e3-140">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="f08e3-141">新-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="f08e3-141">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: dcb5913176af352c39867f7029523765aca0d781
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796234"
---
# <span data-ttu-id="86da7-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="86da7-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="86da7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="86da7-102">SYNOPSIS</span></span>
<span data-ttu-id="86da7-103">取得 VMImage 發行者。</span><span class="sxs-lookup"><span data-stu-id="86da7-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="86da7-104">句法</span><span class="sxs-lookup"><span data-stu-id="86da7-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86da7-105">說明</span><span class="sxs-lookup"><span data-stu-id="86da7-105">DESCRIPTION</span></span>
<span data-ttu-id="86da7-106">**AzVMImagePublisher** Cmdlet 會取得 VMImage 發行者。</span><span class="sxs-lookup"><span data-stu-id="86da7-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="86da7-107">示例</span><span class="sxs-lookup"><span data-stu-id="86da7-107">EXAMPLES</span></span>

### <span data-ttu-id="86da7-108">範例1：為區域取得 VMImage 發行者</span><span class="sxs-lookup"><span data-stu-id="86da7-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="86da7-109">這個命令會在您的 Azure 設定檔中取得美國中部地區的 VMImage 實例發行者。</span><span class="sxs-lookup"><span data-stu-id="86da7-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="86da7-110">參數</span><span class="sxs-lookup"><span data-stu-id="86da7-110">PARAMETERS</span></span>

### <span data-ttu-id="86da7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86da7-111">-DefaultProfile</span></span>
<span data-ttu-id="86da7-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="86da7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86da7-113">-位置</span><span class="sxs-lookup"><span data-stu-id="86da7-113">-Location</span></span>
<span data-ttu-id="86da7-114">指定 VMImage 的位置。</span><span class="sxs-lookup"><span data-stu-id="86da7-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="86da7-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86da7-115">CommonParameters</span></span>
<span data-ttu-id="86da7-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="86da7-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86da7-117">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="86da7-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86da7-118">輸入</span><span class="sxs-lookup"><span data-stu-id="86da7-118">INPUTS</span></span>

### <span data-ttu-id="86da7-119">所有</span><span class="sxs-lookup"><span data-stu-id="86da7-119">None</span></span>
<span data-ttu-id="86da7-120">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="86da7-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="86da7-121">輸出</span><span class="sxs-lookup"><span data-stu-id="86da7-121">OUTPUTS</span></span>

### <span data-ttu-id="86da7-122">PSVirtualMachineImagePublisher 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="86da7-122">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="86da7-123">筆記</span><span class="sxs-lookup"><span data-stu-id="86da7-123">NOTES</span></span>

## <span data-ttu-id="86da7-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="86da7-124">RELATED LINKS</span></span>

[<span data-ttu-id="86da7-125">AzVMImage</span><span class="sxs-lookup"><span data-stu-id="86da7-125">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="86da7-126">AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="86da7-126">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="86da7-127">AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="86da7-127">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="86da7-128">儲存-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="86da7-128">Save-AzVMImage</span></span>](./Save-AzVMImage.md)



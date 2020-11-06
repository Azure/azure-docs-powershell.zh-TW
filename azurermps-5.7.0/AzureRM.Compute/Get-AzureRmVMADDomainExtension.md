---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
ms.openlocfilehash: d55d84560ca75a508a05276d8d33eb78d1d50ab5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449943"
---
# <span data-ttu-id="c41c1-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="c41c1-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="c41c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c41c1-102">SYNOPSIS</span></span>
<span data-ttu-id="c41c1-103">取得有關 AD 網域延伸的資訊。</span><span class="sxs-lookup"><span data-stu-id="c41c1-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c41c1-104">句法</span><span class="sxs-lookup"><span data-stu-id="c41c1-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="c41c1-105">說明</span><span class="sxs-lookup"><span data-stu-id="c41c1-105">DESCRIPTION</span></span>
<span data-ttu-id="c41c1-106">**AzureRmVMADDomainExtension** Cmdlet 會取得指定 Azure Active DIRECTORY (AD) 網域延伸的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c41c1-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="c41c1-107">示例</span><span class="sxs-lookup"><span data-stu-id="c41c1-107">EXAMPLES</span></span>

## <span data-ttu-id="c41c1-108">參數</span><span class="sxs-lookup"><span data-stu-id="c41c1-108">PARAMETERS</span></span>

### <span data-ttu-id="c41c1-109">-名稱</span><span class="sxs-lookup"><span data-stu-id="c41c1-109">-Name</span></span>
<span data-ttu-id="c41c1-110">指定網域延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="c41c1-110">Specifies the name of the domain extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c41c1-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c41c1-111">-ResourceGroupName</span></span>
<span data-ttu-id="c41c1-112">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c41c1-112">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c41c1-113">-狀態</span><span class="sxs-lookup"><span data-stu-id="c41c1-113">-Status</span></span>
<span data-ttu-id="c41c1-114">表示此 Cmdlet 會取得網域延伸的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="c41c1-114">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c41c1-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="c41c1-115">-VMName</span></span>
<span data-ttu-id="c41c1-116">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c41c1-116">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c41c1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c41c1-117">CommonParameters</span></span>
<span data-ttu-id="c41c1-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c41c1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c41c1-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c41c1-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c41c1-120">輸入</span><span class="sxs-lookup"><span data-stu-id="c41c1-120">INPUTS</span></span>

### <span data-ttu-id="c41c1-121">所有</span><span class="sxs-lookup"><span data-stu-id="c41c1-121">None</span></span>
<span data-ttu-id="c41c1-122">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="c41c1-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c41c1-123">輸出</span><span class="sxs-lookup"><span data-stu-id="c41c1-123">OUTPUTS</span></span>

## <span data-ttu-id="c41c1-124">筆記</span><span class="sxs-lookup"><span data-stu-id="c41c1-124">NOTES</span></span>

## <span data-ttu-id="c41c1-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="c41c1-125">RELATED LINKS</span></span>

[<span data-ttu-id="c41c1-126">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="c41c1-126">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)



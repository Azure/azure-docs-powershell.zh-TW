---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaddomainextension
schema: 2.0.0
ms.openlocfilehash: 01a5a69053cfd05186abae45d5b53fff0b022b98
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800553"
---
# <span data-ttu-id="ad3be-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="ad3be-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="ad3be-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ad3be-102">SYNOPSIS</span></span>
<span data-ttu-id="ad3be-103">取得有關 AD 網域延伸的資訊。</span><span class="sxs-lookup"><span data-stu-id="ad3be-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad3be-104">句法</span><span class="sxs-lookup"><span data-stu-id="ad3be-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad3be-105">說明</span><span class="sxs-lookup"><span data-stu-id="ad3be-105">DESCRIPTION</span></span>
<span data-ttu-id="ad3be-106">**AzureRmVMADDomainExtension** Cmdlet 會取得指定 Azure Active DIRECTORY (AD) 網域延伸的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ad3be-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="ad3be-107">示例</span><span class="sxs-lookup"><span data-stu-id="ad3be-107">EXAMPLES</span></span>

### <span data-ttu-id="ad3be-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="ad3be-108">1:</span></span>
```

```

## <span data-ttu-id="ad3be-109">參數</span><span class="sxs-lookup"><span data-stu-id="ad3be-109">PARAMETERS</span></span>

### <span data-ttu-id="ad3be-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad3be-110">-DefaultProfile</span></span>
<span data-ttu-id="ad3be-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ad3be-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad3be-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="ad3be-112">-Name</span></span>
<span data-ttu-id="ad3be-113">指定網域延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad3be-113">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="ad3be-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad3be-114">-ResourceGroupName</span></span>
<span data-ttu-id="ad3be-115">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad3be-115">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ad3be-116">-狀態</span><span class="sxs-lookup"><span data-stu-id="ad3be-116">-Status</span></span>
<span data-ttu-id="ad3be-117">表示此 Cmdlet 會取得網域延伸的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="ad3be-117">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="ad3be-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="ad3be-118">-VMName</span></span>
<span data-ttu-id="ad3be-119">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad3be-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="ad3be-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad3be-120">CommonParameters</span></span>
<span data-ttu-id="ad3be-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ad3be-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad3be-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ad3be-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad3be-123">輸入</span><span class="sxs-lookup"><span data-stu-id="ad3be-123">INPUTS</span></span>

### <span data-ttu-id="ad3be-124">所有</span><span class="sxs-lookup"><span data-stu-id="ad3be-124">None</span></span>
<span data-ttu-id="ad3be-125">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="ad3be-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ad3be-126">輸出</span><span class="sxs-lookup"><span data-stu-id="ad3be-126">OUTPUTS</span></span>

### <span data-ttu-id="ad3be-127">VirtualMachineADDomainExtensionCoNtext 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="ad3be-127">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="ad3be-128">筆記</span><span class="sxs-lookup"><span data-stu-id="ad3be-128">NOTES</span></span>

## <span data-ttu-id="ad3be-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad3be-129">RELATED LINKS</span></span>

[<span data-ttu-id="ad3be-130">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="ad3be-130">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
ms.openlocfilehash: 809246520c4e6b07a1aca406ef3ec17eb9df31f1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796285"
---
# <span data-ttu-id="0ae1d-101">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="0ae1d-101">Get-AzVMADDomainExtension</span></span>

## <span data-ttu-id="0ae1d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0ae1d-102">SYNOPSIS</span></span>
<span data-ttu-id="0ae1d-103">取得有關 AD 網域延伸的資訊。</span><span class="sxs-lookup"><span data-stu-id="0ae1d-103">Gets information about an AD domain extension.</span></span>

## <span data-ttu-id="0ae1d-104">句法</span><span class="sxs-lookup"><span data-stu-id="0ae1d-104">SYNTAX</span></span>

```
Get-AzVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ae1d-105">說明</span><span class="sxs-lookup"><span data-stu-id="0ae1d-105">DESCRIPTION</span></span>
<span data-ttu-id="0ae1d-106">**AzVMADDomainExtension** Cmdlet 會取得指定 Azure Active DIRECTORY (AD) 網域延伸的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0ae1d-106">The **Get-AzVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="0ae1d-107">示例</span><span class="sxs-lookup"><span data-stu-id="0ae1d-107">EXAMPLES</span></span>

### <span data-ttu-id="0ae1d-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="0ae1d-108">1:</span></span>
```

```

## <span data-ttu-id="0ae1d-109">參數</span><span class="sxs-lookup"><span data-stu-id="0ae1d-109">PARAMETERS</span></span>

### <span data-ttu-id="0ae1d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ae1d-110">-DefaultProfile</span></span>
<span data-ttu-id="0ae1d-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0ae1d-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ae1d-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="0ae1d-112">-Name</span></span>
<span data-ttu-id="0ae1d-113">指定網域延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ae1d-113">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="0ae1d-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ae1d-114">-ResourceGroupName</span></span>
<span data-ttu-id="0ae1d-115">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ae1d-115">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0ae1d-116">-狀態</span><span class="sxs-lookup"><span data-stu-id="0ae1d-116">-Status</span></span>
<span data-ttu-id="0ae1d-117">表示此 Cmdlet 會取得網域延伸的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="0ae1d-117">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="0ae1d-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="0ae1d-118">-VMName</span></span>
<span data-ttu-id="0ae1d-119">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ae1d-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="0ae1d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ae1d-120">CommonParameters</span></span>
<span data-ttu-id="0ae1d-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0ae1d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ae1d-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0ae1d-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ae1d-123">輸入</span><span class="sxs-lookup"><span data-stu-id="0ae1d-123">INPUTS</span></span>

### <span data-ttu-id="0ae1d-124">所有</span><span class="sxs-lookup"><span data-stu-id="0ae1d-124">None</span></span>
<span data-ttu-id="0ae1d-125">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="0ae1d-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0ae1d-126">輸出</span><span class="sxs-lookup"><span data-stu-id="0ae1d-126">OUTPUTS</span></span>

### <span data-ttu-id="0ae1d-127">VirtualMachineADDomainExtensionCoNtext 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="0ae1d-127">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="0ae1d-128">筆記</span><span class="sxs-lookup"><span data-stu-id="0ae1d-128">NOTES</span></span>

## <span data-ttu-id="0ae1d-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="0ae1d-129">RELATED LINKS</span></span>

[<span data-ttu-id="0ae1d-130">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="0ae1d-130">Set-AzVMADDomainExtension</span></span>](./Set-AzVMADDomainExtension.md)



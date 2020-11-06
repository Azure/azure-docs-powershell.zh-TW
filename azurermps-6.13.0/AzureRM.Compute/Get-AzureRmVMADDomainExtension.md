---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
ms.openlocfilehash: 398cc4b8f23ca5296aec741eb720833f589b0e2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447434"
---
# <span data-ttu-id="8d481-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="8d481-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="8d481-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8d481-102">SYNOPSIS</span></span>
<span data-ttu-id="8d481-103">取得有關 AD 網域延伸的資訊。</span><span class="sxs-lookup"><span data-stu-id="8d481-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d481-104">句法</span><span class="sxs-lookup"><span data-stu-id="8d481-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d481-105">說明</span><span class="sxs-lookup"><span data-stu-id="8d481-105">DESCRIPTION</span></span>
<span data-ttu-id="8d481-106">**AzureRmVMADDomainExtension** Cmdlet 會取得指定 Azure Active DIRECTORY (AD) 網域延伸的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8d481-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="8d481-107">示例</span><span class="sxs-lookup"><span data-stu-id="8d481-107">EXAMPLES</span></span>

## <span data-ttu-id="8d481-108">參數</span><span class="sxs-lookup"><span data-stu-id="8d481-108">PARAMETERS</span></span>

### <span data-ttu-id="8d481-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d481-109">-DefaultProfile</span></span>
<span data-ttu-id="8d481-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8d481-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d481-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="8d481-111">-Name</span></span>
<span data-ttu-id="8d481-112">指定網域延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d481-112">Specifies the name of the domain extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d481-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d481-113">-ResourceGroupName</span></span>
<span data-ttu-id="8d481-114">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d481-114">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d481-115">-狀態</span><span class="sxs-lookup"><span data-stu-id="8d481-115">-Status</span></span>
<span data-ttu-id="8d481-116">表示此 Cmdlet 會取得網域延伸的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="8d481-116">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d481-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="8d481-117">-VMName</span></span>
<span data-ttu-id="8d481-118">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d481-118">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d481-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d481-119">CommonParameters</span></span>
<span data-ttu-id="8d481-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8d481-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d481-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8d481-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d481-122">輸入</span><span class="sxs-lookup"><span data-stu-id="8d481-122">INPUTS</span></span>

### <span data-ttu-id="8d481-123">System.object</span><span class="sxs-lookup"><span data-stu-id="8d481-123">System.String</span></span>

### <span data-ttu-id="8d481-124">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="8d481-124">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8d481-125">輸出</span><span class="sxs-lookup"><span data-stu-id="8d481-125">OUTPUTS</span></span>

### <span data-ttu-id="8d481-126">VirtualMachineADDomainExtensionCoNtext 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="8d481-126">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="8d481-127">筆記</span><span class="sxs-lookup"><span data-stu-id="8d481-127">NOTES</span></span>

## <span data-ttu-id="8d481-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d481-128">RELATED LINKS</span></span>

[<span data-ttu-id="8d481-129">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="8d481-129">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)



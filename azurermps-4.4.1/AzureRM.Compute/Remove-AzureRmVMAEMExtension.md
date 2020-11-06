---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
ms.openlocfilehash: e75c34d76c304af272655c3e4e81fcfd547d11b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452527"
---
# <span data-ttu-id="6e4d4-101">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="6e4d4-101">Remove-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="6e4d4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6e4d4-102">SYNOPSIS</span></span>
<span data-ttu-id="6e4d4-103">從虛擬機器中移除 AEM 延伸功能。</span><span class="sxs-lookup"><span data-stu-id="6e4d4-103">Removes the AEM extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e4d4-104">句法</span><span class="sxs-lookup"><span data-stu-id="6e4d4-104">SYNTAX</span></span>

```
Remove-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e4d4-105">說明</span><span class="sxs-lookup"><span data-stu-id="6e4d4-105">DESCRIPTION</span></span>
<span data-ttu-id="6e4d4-106">**AzureRmVMAEMExtension** Cmdlet 會將 Azure 增強型監視 (AEM) 延伸從虛擬機器中移除。</span><span class="sxs-lookup"><span data-stu-id="6e4d4-106">The **Remove-AzureRmVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="6e4d4-107">示例</span><span class="sxs-lookup"><span data-stu-id="6e4d4-107">EXAMPLES</span></span>

### <span data-ttu-id="6e4d4-108">範例1：移除 AEM 延伸</span><span class="sxs-lookup"><span data-stu-id="6e4d4-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="6e4d4-109">這個命令會移除名為 contoso-server 的虛擬機器的 AEM 延伸功能。</span><span class="sxs-lookup"><span data-stu-id="6e4d4-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="6e4d4-110">參數</span><span class="sxs-lookup"><span data-stu-id="6e4d4-110">PARAMETERS</span></span>

### <span data-ttu-id="6e4d4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e4d4-111">-DefaultProfile</span></span>
<span data-ttu-id="6e4d4-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6e4d4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e4d4-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="6e4d4-113">-Name</span></span>
<span data-ttu-id="6e4d4-114">指定此 Cmdlet 從中移除 AEM 延伸的虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e4d4-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e4d4-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="6e4d4-115">-OSType</span></span>
<span data-ttu-id="6e4d4-116">指定作業系統磁片作業系統的類型。</span><span class="sxs-lookup"><span data-stu-id="6e4d4-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="6e4d4-117">如果作業系統磁片沒有類型，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="6e4d4-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="6e4d4-118">此參數可接受的值為： Windows 和 Linux。</span><span class="sxs-lookup"><span data-stu-id="6e4d4-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e4d4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e4d4-119">-ResourceGroupName</span></span>
<span data-ttu-id="6e4d4-120">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e4d4-120">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="6e4d4-121">這個 Cmdlet 會從該虛擬機器中移除 AEM 延伸。</span><span class="sxs-lookup"><span data-stu-id="6e4d4-121">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="6e4d4-122">-VMName</span><span class="sxs-lookup"><span data-stu-id="6e4d4-122">-VMName</span></span>
<span data-ttu-id="6e4d4-123">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e4d4-123">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="6e4d4-124">這個 Cmdlet 會移除此參數指定之虛擬機器的 AEM 延伸。</span><span class="sxs-lookup"><span data-stu-id="6e4d4-124">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="6e4d4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e4d4-125">CommonParameters</span></span>
<span data-ttu-id="6e4d4-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6e4d4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e4d4-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6e4d4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e4d4-128">輸入</span><span class="sxs-lookup"><span data-stu-id="6e4d4-128">INPUTS</span></span>

## <span data-ttu-id="6e4d4-129">輸出</span><span class="sxs-lookup"><span data-stu-id="6e4d4-129">OUTPUTS</span></span>

## <span data-ttu-id="6e4d4-130">筆記</span><span class="sxs-lookup"><span data-stu-id="6e4d4-130">NOTES</span></span>

## <span data-ttu-id="6e4d4-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="6e4d4-131">RELATED LINKS</span></span>

[<span data-ttu-id="6e4d4-132">AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="6e4d4-132">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="6e4d4-133">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="6e4d4-133">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="6e4d4-134">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="6e4d4-134">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)



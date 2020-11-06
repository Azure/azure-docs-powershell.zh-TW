---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: f074d61919098d6c23ab39424774d9ba18e457d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446364"
---
# <span data-ttu-id="3a478-101">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="3a478-101">Remove-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="3a478-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3a478-102">SYNOPSIS</span></span>
<span data-ttu-id="3a478-103">從虛擬機器移除 SQL Server 延伸。</span><span class="sxs-lookup"><span data-stu-id="3a478-103">Removes a SQL Server extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a478-104">句法</span><span class="sxs-lookup"><span data-stu-id="3a478-104">SYNTAX</span></span>

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="3a478-105">說明</span><span class="sxs-lookup"><span data-stu-id="3a478-105">DESCRIPTION</span></span>
<span data-ttu-id="3a478-106">**AzureRmVMSqlServerExtension** Cmdlet 會從虛擬機器中移除 AzureSQL 伺服器延伸。</span><span class="sxs-lookup"><span data-stu-id="3a478-106">The **Remove-AzureRmVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="3a478-107">示例</span><span class="sxs-lookup"><span data-stu-id="3a478-107">EXAMPLES</span></span>

### <span data-ttu-id="3a478-108">範例1：移除 SQL Server 延伸</span><span class="sxs-lookup"><span data-stu-id="3a478-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="3a478-109">這個命令會從名為 ContosoVM22 的虛擬機器中移除 SQL Server 延伸。</span><span class="sxs-lookup"><span data-stu-id="3a478-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="3a478-110">參數</span><span class="sxs-lookup"><span data-stu-id="3a478-110">PARAMETERS</span></span>

### <span data-ttu-id="3a478-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="3a478-111">-Name</span></span>
<span data-ttu-id="3a478-112">指定此 Cmdlet 移除之副檔名之 SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a478-112">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3a478-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a478-113">-ResourceGroupName</span></span>
<span data-ttu-id="3a478-114">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a478-114">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3a478-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="3a478-115">-VMName</span></span>
<span data-ttu-id="3a478-116">指定此 Cmdlet 從中移除 SQL Server 延伸的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="3a478-116">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="3a478-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a478-117">CommonParameters</span></span>
<span data-ttu-id="3a478-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3a478-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a478-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3a478-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a478-120">輸入</span><span class="sxs-lookup"><span data-stu-id="3a478-120">INPUTS</span></span>

### <span data-ttu-id="3a478-121">所有</span><span class="sxs-lookup"><span data-stu-id="3a478-121">None</span></span>
<span data-ttu-id="3a478-122">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="3a478-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3a478-123">輸出</span><span class="sxs-lookup"><span data-stu-id="3a478-123">OUTPUTS</span></span>

## <span data-ttu-id="3a478-124">筆記</span><span class="sxs-lookup"><span data-stu-id="3a478-124">NOTES</span></span>

## <span data-ttu-id="3a478-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a478-125">RELATED LINKS</span></span>

[<span data-ttu-id="3a478-126">AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="3a478-126">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="3a478-127">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="3a478-127">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)



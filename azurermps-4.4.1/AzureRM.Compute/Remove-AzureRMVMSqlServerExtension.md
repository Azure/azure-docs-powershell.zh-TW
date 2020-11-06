---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: 19d4022fcf5f3eee0ee8d77e7c061ae2f8d00629
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455855"
---
# <span data-ttu-id="33e57-101">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="33e57-101">Remove-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="33e57-102">摘要</span><span class="sxs-lookup"><span data-stu-id="33e57-102">SYNOPSIS</span></span>
<span data-ttu-id="33e57-103">從虛擬機器移除 SQL Server 延伸。</span><span class="sxs-lookup"><span data-stu-id="33e57-103">Removes a SQL Server extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33e57-104">句法</span><span class="sxs-lookup"><span data-stu-id="33e57-104">SYNTAX</span></span>

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33e57-105">說明</span><span class="sxs-lookup"><span data-stu-id="33e57-105">DESCRIPTION</span></span>
<span data-ttu-id="33e57-106">**AzureRmVMSqlServerExtension** Cmdlet 會從虛擬機器中移除 AzureSQL 伺服器延伸。</span><span class="sxs-lookup"><span data-stu-id="33e57-106">The **Remove-AzureRmVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="33e57-107">示例</span><span class="sxs-lookup"><span data-stu-id="33e57-107">EXAMPLES</span></span>

### <span data-ttu-id="33e57-108">範例1：移除 SQL Server 延伸</span><span class="sxs-lookup"><span data-stu-id="33e57-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="33e57-109">這個命令會從名為 ContosoVM22 的虛擬機器中移除 SQL Server 延伸。</span><span class="sxs-lookup"><span data-stu-id="33e57-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="33e57-110">參數</span><span class="sxs-lookup"><span data-stu-id="33e57-110">PARAMETERS</span></span>

### <span data-ttu-id="33e57-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33e57-111">-DefaultProfile</span></span>
<span data-ttu-id="33e57-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="33e57-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33e57-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="33e57-113">-Name</span></span>
<span data-ttu-id="33e57-114">指定此 Cmdlet 移除之副檔名之 SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="33e57-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="33e57-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33e57-115">-ResourceGroupName</span></span>
<span data-ttu-id="33e57-116">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="33e57-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="33e57-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="33e57-117">-VMName</span></span>
<span data-ttu-id="33e57-118">指定此 Cmdlet 從中移除 SQL Server 延伸的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="33e57-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="33e57-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33e57-119">CommonParameters</span></span>
<span data-ttu-id="33e57-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="33e57-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33e57-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="33e57-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33e57-122">輸入</span><span class="sxs-lookup"><span data-stu-id="33e57-122">INPUTS</span></span>

## <span data-ttu-id="33e57-123">輸出</span><span class="sxs-lookup"><span data-stu-id="33e57-123">OUTPUTS</span></span>

## <span data-ttu-id="33e57-124">筆記</span><span class="sxs-lookup"><span data-stu-id="33e57-124">NOTES</span></span>

## <span data-ttu-id="33e57-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="33e57-125">RELATED LINKS</span></span>

[<span data-ttu-id="33e57-126">AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="33e57-126">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="33e57-127">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="33e57-127">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)



---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: a6f2ed82835cca252f905cb53c5ddd9c8530900a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455511"
---
# <span data-ttu-id="69cf4-101">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="69cf4-101">Get-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="69cf4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="69cf4-102">SYNOPSIS</span></span>
<span data-ttu-id="69cf4-103">取得虛擬機器上的 SQL Server 延伸設定。</span><span class="sxs-lookup"><span data-stu-id="69cf4-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69cf4-104">句法</span><span class="sxs-lookup"><span data-stu-id="69cf4-104">SYNTAX</span></span>

```
Get-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="69cf4-105">說明</span><span class="sxs-lookup"><span data-stu-id="69cf4-105">DESCRIPTION</span></span>
<span data-ttu-id="69cf4-106">**AzureRmVMSqlServerExtension** Cmdlet 會取得 SQL Server 基礎結構的設定，成為虛擬機器上的服務 (IaaS) 代理程式。</span><span class="sxs-lookup"><span data-stu-id="69cf4-106">The **Get-AzureRmVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="69cf4-107">示例</span><span class="sxs-lookup"><span data-stu-id="69cf4-107">EXAMPLES</span></span>

### <span data-ttu-id="69cf4-108">範例1：在虛擬機器上取得 SQL Server 延伸設定</span><span class="sxs-lookup"><span data-stu-id="69cf4-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="69cf4-109">這個命令會取得名為 ContosoVM07 的虛擬機器上的 SQL Server 延伸設定。</span><span class="sxs-lookup"><span data-stu-id="69cf4-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="69cf4-110">範例2：使用管線取得設定</span><span class="sxs-lookup"><span data-stu-id="69cf4-110">Example 2: Get the settings by using the pipeline</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service08" -Name "ContosoVM22" | Get-AzureRmVMSqlServerExtension
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="69cf4-111">這個命令會透過使用 Get-AzureRmVM Cmdlet，在服務 Service08 上取得名為 ContosoVM22 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="69cf4-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="69cf4-112">命令會使用管線運算子，將結果傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="69cf4-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="69cf4-113">目前的命令會取得該虛擬機器上的 SQL Server IaaS 代理程式設定。</span><span class="sxs-lookup"><span data-stu-id="69cf4-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="69cf4-114">範例3：取得特定 SQL Server 版本的設定</span><span class="sxs-lookup"><span data-stu-id="69cf4-114">Example 3: Get the settings of specific SQL Server version</span></span>
```
PS C:\> Get-AzureRmVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07" -Version "1.0"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="69cf4-115">這個命令會在名為 ContosoVM07 的虛擬機器上，取得 SQL Server 延伸版本1.0 的設定。</span><span class="sxs-lookup"><span data-stu-id="69cf4-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="69cf4-116">參數</span><span class="sxs-lookup"><span data-stu-id="69cf4-116">PARAMETERS</span></span>

### <span data-ttu-id="69cf4-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="69cf4-117">-Name</span></span>
<span data-ttu-id="69cf4-118">指定副檔名的 SQL 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="69cf4-118">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="69cf4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69cf4-119">-ResourceGroupName</span></span>
<span data-ttu-id="69cf4-120">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="69cf4-120">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="69cf4-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="69cf4-121">-VMName</span></span>
<span data-ttu-id="69cf4-122">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="69cf4-122">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="69cf4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69cf4-123">CommonParameters</span></span>
<span data-ttu-id="69cf4-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="69cf4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69cf4-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="69cf4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69cf4-126">輸入</span><span class="sxs-lookup"><span data-stu-id="69cf4-126">INPUTS</span></span>

### <span data-ttu-id="69cf4-127">所有</span><span class="sxs-lookup"><span data-stu-id="69cf4-127">None</span></span>
<span data-ttu-id="69cf4-128">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="69cf4-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="69cf4-129">輸出</span><span class="sxs-lookup"><span data-stu-id="69cf4-129">OUTPUTS</span></span>

## <span data-ttu-id="69cf4-130">筆記</span><span class="sxs-lookup"><span data-stu-id="69cf4-130">NOTES</span></span>

## <span data-ttu-id="69cf4-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="69cf4-131">RELATED LINKS</span></span>

[<span data-ttu-id="69cf4-132">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="69cf4-132">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="69cf4-133">移除-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="69cf4-133">Remove-AzureRmVMSqlServerExtension</span></span>](./Remove-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="69cf4-134">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="69cf4-134">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


